pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test -- --watch=false'
      }
    }

    stage('Manual Approval') {
      steps {
        input message: 'Lanjutkan ke tahap Deploy?'
      }
    }

    stage('Deploy') {
      steps {
        sh 'npm start &'
        sleep(time: 1, unit: 'MINUTES')
      }
    }
  }
}
