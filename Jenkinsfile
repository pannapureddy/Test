pipeline {
    agent any
    tools { nodejs "NodeJS" }
    stages {
        stage('Checkout') {
            steps {
                sshagent(['bf5144c870928000792010f351c52a8d050f8dbd']) {
                    git url: "git@github.com:pannapureddy/Test.git"
                }
            }
        }

        stage('build') {
            steps {
                sh "npm config ls"
                sh "npm install"
            }
        }

        stage('Development') {
            when {
                branch 'develop'
            }
            steps {
                sh "echo 'Development'"
            }
        }

        stage('Production') {
            when {
                branch 'master'
            }
            steps {
                sh "echo 'Production'"
            }
        }
    }
}
