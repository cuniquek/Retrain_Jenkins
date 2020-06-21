pipeline {
   agent any
   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/cuniquek/Retrain_Jenkins.git'

            
            sh "vi jenkinsfile"
         }

         post {
            // If Maven was able to run the tests, even if some of the test
            // failed, record the test results and archive the jar file.
            success {
             sh "echo "Jenkins" > ./presentation.txt"  
            }
         }
      }
   }
}

