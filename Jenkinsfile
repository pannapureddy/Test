pipeline {
    agent any
    tools { nodejs "NodeJS" }
    stages {
        stage('Checkout') {
            steps {
                sshagent(['bf5144c870928000792010f351c52a8d050f8dbd']) {
                    git url: "git@github.com:pannapureddy/Test.git", branch: "develop"
                }
            }
        }

        stage('Build') {
            steps {
                sh "npm config ls"
                sh "npm install"
                sh "npm start"
            }
        }
    }
}
