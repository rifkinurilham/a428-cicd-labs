pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                  npm install
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                  echo "skip test"
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                  echo "deploying app..."
                  npm run build || true
                '''
            }
        }
    }
}

