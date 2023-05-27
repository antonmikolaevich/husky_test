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
                bat 'npm run wdio'
            }
        }
    }
}