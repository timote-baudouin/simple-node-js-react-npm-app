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
        sh 'echo "coucou"'
      }
    }

    stage('install') {
      steps {
        sh '''npm install
'''
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
export PATH="$(yarn global bin):$PATH
'''
      }
    }

  }
  environment {
    FIREBASE_TOKEN = '1//03I2JIEziVvH3CgYIARAAGAMSNwF-L9IrgIoYHW_nS52FMKNO2-Cy9cdtNoJcwk-PJIQF0HgO-xEphKvfCwuX3AZso1MA7xZG5Ks'
  }
}