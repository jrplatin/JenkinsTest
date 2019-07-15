pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        /* "Build" and "Test" stages omitted */

        stage('Deploy - Staging') {
            steps {
                sh 'print("hello world")'
                sh 'print("2")'
            }
        }

        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }

        stage('Deploy - Production') {
            steps {
                sh 'print("aa")'
            }
        }
    }
}
