node {
    stage('Checkout') {
        sshagent(['bf5144c870928000792010f351c52a8d050f8dbd']) {
            git url: "git@github.com:pannapureddy/Test.git", branch: "develop"
        }
    }

    stage('Build') {
        agent any
        steps {
            withNpm(npmConfig: 'my-custom-npmrc') {
                sh "npm install"
                sh "npm test"
            }
        }
    }
}
