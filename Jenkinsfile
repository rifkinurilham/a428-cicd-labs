pipeline {
  agent any

  tools {
    nodejs 'node18'
  }

  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test || true'
      }
    }

 stage('Manual Approval') {
      steps {
        input message: 'Lanjutkan ke tahap Deploy?'
      }
    }

stage('Deploy') {
  steps {
    sh '''
      echo "Aplikasi berjalan..."
      sleep 60
      echo "Aplikasi berhenti otomatis"
    '''
  }
}


  }
}
