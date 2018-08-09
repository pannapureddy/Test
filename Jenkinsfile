node {
    stage('Checkout') {
        sshagent(['bf5144c870928000792010f351c52a8d050f8dbd']) {
            git url: "git@github.com:pannapureddy/Test.git", branch: "develop"
        }
    }

    stage('Build') {
        agent any
        sh "echo `DO NPM STUFF.....`"
    }
}
