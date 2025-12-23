pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build || echo "No build script"'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "No test available"'
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
                  echo "Deploying application..."
                  npm start &
                  sleep 60
                  echo "Application stopped after 1 minute"
                '''
            }
        }
    }
}
