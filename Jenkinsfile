pipeline {
   agent any
   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/cuniquek/Retrain_Jenkins.git' 
            sh "ls"
         }

         post {
            // If Maven was able to run the tests, even if some of the test
            // failed, record the test results and archive the jar file.
            success {
             sh "echo 'Jenkins'>./presentation.txt"
             sh "git config --global user.email 'kkaps@intracom-telecom.com'"
             sh "git config --global user.name 'Konstantinos Kapsalis'"
             sh "git add ."
             sh "git commit -m 'Jenkins was here!!'"
             sh "git push"
            }
         }
      }
   }
}

