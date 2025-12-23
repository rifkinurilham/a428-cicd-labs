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
                sh 'npm test -- --watch=false'
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
            echo "Install dependency"
            npm install

            echo "Jalanin aplikasi"
            npm start &
            sleep 60

            echo "Udah 1 menit, selesai" 
            }
        }
    }
}
