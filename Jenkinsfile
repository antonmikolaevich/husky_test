pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }

        stage('UI') {
            steps {
                bat 'npm run test'
            }
        }
    }
    post {
        always {
            junit allowEmptyResults: true, testResults: '*.xml'
            archiveArtifacts artifacts: '*.xml'
        }
    }
}