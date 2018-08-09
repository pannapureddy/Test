node {
  stage('Checkout') {
      sh "eval ssh-agent -s"
      sh "ssh-add -K ~/.ssh/id_rsa"
      git url: "git@github.com:pannapureddy/Test.git", branch: "develop"
  }


  stage('Build') {
      def nodeHome = tool name: 'nodejs', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
      env.PATH = "${nodeHome}/bin:${env.PATH}"
      sh "npm install"
      sh "npm test"  
  }
}
