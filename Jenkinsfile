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

         post {
            // If Maven was able to run the tests, even if some of the test
            // failed, record the test results and archive the jar file.
            success {
             sh "echo 'Jenkins'>./presentation.txt"
             sh 'git config --global user.email "kostas87_tzes@hotmail.com"'
             sh 'git config --global user.name "cuniquek"'
             sh 'git remote add origin https://cuniquek:lathossxoli17@github.com/cuniquek/Retrain_Jenkins.git'
             sh "git add ."
             sh 'git commit -m "Jenkins was here!!"'
             sh "git push --set-upstream origin development"
            }
         }
      }
   }
}

