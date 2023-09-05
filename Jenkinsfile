pipeline {
  agent {
    docker {
      image 'node:18.17.1-alpine3.18'
      args ' -p 3000:3000'
    }

  }
  stages {
    stage('welcome') {
      steps {
        sh 'echo "bonjour"'
      }
    }

    stage('install') {
      steps {
        sh 'npm install'
      }
    }

    stage('build') {
      steps {
        sh 'npm run build'
      }
    }

    stage('deploy') {
      steps {
        sh '''yarn global add firebase-tools
echo FIREBASE_TOKEN
export PATH="$(yarn global bin):$PATH"
firebase deploy --only hosting:briefcicdbaudouintimote --project jenkin-blueocean-pipeline --token $FIREBASE_TOKEN'''
      }
    }

  }
  environment {
    FIREBASE_TOKEN = '1//03eEzCNtknD4nCgYIARAAGAMSNwF-L9IrQWsmt3ZyCLAxl82keBiDuEDva_AJUzkKCRjTZrZH2xb9_k3h3XbZgbRiWc70FhRxNRc'
  }
}