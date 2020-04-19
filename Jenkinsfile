pipeline {
    agent { docker { image 'node:latest' } }
    stages {
      stage('build') {
        steps {
          sh 'ls -l'
          sh 'npm ci'
          sh 'npm test'
        }
        steps {
          sh 'npm build'
        }
      }
    }
}