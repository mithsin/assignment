pipeline {
    agent any
    stages {

        stage('test'){
            steps {
              bat 'set -x
              # npm install --save-dev cross-env
              set +x'
            }
        }
       stage ('start'){
            steps {
              bat 'set -x
              npm run build
              set +x'
            }
       }
       stage ('deploy'){
            steps {
                bat 'npm start &
              sleep 1
              echo $! > .pidfile'
            }
       }
    }
}
