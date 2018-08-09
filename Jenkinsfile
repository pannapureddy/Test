node {
  stage('Checkout') {
      git url: env.GITBUCKET_URL + "/wey-yu/hello.git", branch: env.BRANCH_NAME
  }
 
  stage('Build') {
      def nodeHome = tool name: 'nodejs', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
      env.PATH = "${nodeHome}/bin:${env.PATH}"
      sh "npm install"
      sh "npm test"  
  }
}
