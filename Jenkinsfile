pipeline {
   agent any
   stages{
    stage('Testing commit trigger'){
       steps{
         echo 'Triggering from SCM'
         node --version
         npm --version
       }
    }
   }
}