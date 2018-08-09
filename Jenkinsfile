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

        stage('Development') {
            when {
                branch 'develop'
            }
            steps {
                sh "npm config ls"
                sh "echo 'Development'"
                sh "npm install"
            }
        }

        stage('Production') {
            when {
                branch 'master'
            }
            steps {
                sh "npm config ls"
                sh "echo 'Production'"
                sh "npm install"
            }
        }
    }
}
