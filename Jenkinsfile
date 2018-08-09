node {
  stage('Checkout') {
      git url: "git@github.com:pannapureddy/Test.git", branch: "master"
  }


  stage('Build') {
      def nodeHome = tool name: 'nodejs', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
      env.PATH = "${nodeHome}/bin:${env.PATH}"
      sh "eval $(ssh-agent -s)"
      sh "ssh-add -K ~/.ssh/id_rsa"
      sh "npm install"
      sh "npm test"  
  }
}
