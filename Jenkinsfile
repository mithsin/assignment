pipeline {
    agent any
    stages {

        stage('test'){
            steps {
                bat 'npm test'
            }
        }
       stage ('start'){
            steps {
                bat 'npm start'
            }
       }
    }
}
