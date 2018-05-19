pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {

        stage('Test') {
            steps {
              bat './jfile/test.bat'
            }
        }
        stage('Deliver') {
            steps {
              bat './jfile/deliver.bat'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
              bat './jfile/kill.bat'
            }
        }
    }
}
