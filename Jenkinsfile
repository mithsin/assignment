pipeline {
    agent any
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
              bat './jfile/test.sh'
            }
        }
        stage('Deliver') {
            steps {
              bat './jfile/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
              bat './jfile/kill.sh'
            }
        }
    }
}
