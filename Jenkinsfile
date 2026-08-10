pipeline {
   agent any
   stages{
    stage('Testing commit trigger'){
       steps{
         echo 'Triggering from SCM'
         sh 'node --version'
         sh 'npm --version'
       }
    }
   }
}