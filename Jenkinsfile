pipeline {
    agent { docker { image 'node:latest' } }
    stages {
        stage('build') {
            steps {
                sh 'ls -l'
            }
            steps {
                sh 'npm --version'
            }
            steps {
                sh 'npm ci'
            }
        }
        stage('test') {
            steps {
                sh 'npm test'
            }
        }
    }
}