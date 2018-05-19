pipeline {
    agent any
    stages {
        stage('init-project') {
            steps {
                bat 'npm install'
            }
            steps {   bat 'npm start'
            }
        }
    }
}
