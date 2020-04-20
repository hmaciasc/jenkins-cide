pipeline {
    agent {
        docker {
            image 'node:13-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm ci'
            }
        }
        stage('Test') { 
            steps {
                sh 'npm test' 
            }
        }
        stage('Deliver') { 
            steps {
                sh 'npm build' 
            }
        }
    }
    post {
      success { echo 'Successful build and test' }
    }
}