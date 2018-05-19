pipeline {
    agent any
    stages {
        stage('init-project') {
            steps {
                bat 'npm run build'
            }
        }
        stage('test'){
            steps {
                bat 'npm test'
            }
        }
        stage('start'){
            steps {
                bat 'npm start'
            }
        }
        stage('deploy'){
            steps {
              bat 'npm start'
            }
            steps {
              bat 'sleep 1'
            }
            steps {
              echo '$! > .pidfile'
            }
        }
    }
}
