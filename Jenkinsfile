pipeline {
    agent none
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npm start'
            }
        }
    }
}