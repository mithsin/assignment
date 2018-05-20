pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                bat './jenkins/scripts/test.bat'
            }
        }
        stage('Deliver') {
            steps {
                bat './jenkins/scripts/deliver.bat'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                  bat './jenkins/scripts/kill.bat' 
            }
        }
    }
}
