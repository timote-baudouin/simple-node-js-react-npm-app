pipeline {
  agent {
    docker {
      image 'node:18.17.1-alpine3.18'
      args 'L\'image du conteneur'
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