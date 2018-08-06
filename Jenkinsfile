pipeline {
    agent {
        node {
            label 'running-node'
        }
    }
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