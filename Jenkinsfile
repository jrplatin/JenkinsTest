pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        /* "Build" and "Test" stages omitted */

        stage('Build') {
            steps {
                ./ssh.sh
            }
        }
        
        stage('Test'){
            echo 'Testing...'
            
        }
        stage('Deploy'){
            
            echo 'Done!'
               
        }

        }
    }
}
