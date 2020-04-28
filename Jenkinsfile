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
                sh 'npm build' 
            }
        }
        stage('Test') { 
            steps {
                sh 'npm test' 
            }
        }
        stage('Deploy') { 
            steps {
              echo 'run deploy script to production...'
            }
        }
    }
    post {
      success { echo 'Successful build and test' }
    }
}