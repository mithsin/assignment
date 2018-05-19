pipeline {
    agent any
    stages {
        stage('init-project') {
            steps {
                bat 'npm install'
            }
        }
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
