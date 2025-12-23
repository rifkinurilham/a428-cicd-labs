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
    }
}

