pipeline {
    agent any
    environment {
        EMAIL_ADDRESS = 'jacob.platin@aidoc.com'
    }
    stages {
        stage('No-op') {
            steps {
                sh 'ls'
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            mail to: "${env.EMAIL_ADDRESS}",
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
        }
     
    }
}
