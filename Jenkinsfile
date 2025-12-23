pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

    stage('Test') {
    steps {
        sh 'echo "skip test"'
              } 
        }

        stage('Manual Approval') {
            steps {
                input message: 'Lanjutkan ke tahap Deploy?', ok: 'Proceed'
            }
        }

        stage('Deploy') {
            steps {
               sh '''
        echo "Deploying application..."
        echo "Deploy success 🎉"
        '''
             
            }
        }
    }
}
