pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {

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
