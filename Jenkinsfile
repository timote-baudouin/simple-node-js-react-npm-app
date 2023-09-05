pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:18.17.1-alpine3.18'
    }

  }
  stages {
    stage('welcome') {
      steps {
        sh 'echo "coucou"'
      }
    }

  }
}