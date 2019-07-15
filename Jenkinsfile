pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew check'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
              sh 'ln -s tests/test-results-unit.xml $WORKSPACE'
              junit "build/reports/test-results-unit.xml"
            
        }
    }
}
