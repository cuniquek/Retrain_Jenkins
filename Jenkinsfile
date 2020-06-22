pipeline {
   agent any
   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/cuniquek/Retrain_Jenkins.git'
            sh "git checkout development"
            sh "ls"
         }
      }
      stage('Testing') {
          steps {
              echo 'Hello World!!'
          }
          post {
                success {
                    echo 'success'
                }
                failure {
                    echo 'failure'
                }
            }
      }
    }
}

