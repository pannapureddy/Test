node('testing') {
    stage('Initialize') {
        echo 'Initializing...'
        def node = tool name: 'Node-10.8.0', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
        env.PATH = "${node}/bin:${env.PATH}"
    }
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