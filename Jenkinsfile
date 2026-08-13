// pipeline {
//     agent any
    
//   stages {
//     stage('Docker run npm'){
//         steps {
//             echo 'running node:18-alpine docker image'
//             sh 'docker run node:18-alpine'
//             }
//         }
//     stage('Installing npm packages and dependencies'){
//         steps{
//             echo 'Installing npm packages'
//             sh 'npm install'
//             echo 'Npm packages have been installed successfully'
//             }
//           }
//     stages('Building project'){
//         steps{
//             echo 'Initiating the project build'
//             sh 'npm run build'
//             echo 'Project has been build successfully. Build folder should be available now'
//             }
//         }}



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
    //  stage('Printing current directory and its contents'){
    //    steps{
    //      echo 'Printing the current directory'
    //      sh 'pwd'
    //      echo 'Printing files and folder present there'
    //      echo 'ls -la'
    //    }
    //  }
    stage('Downloading and installing all the npm packages'){
       steps{
        echo 'downloading and installing all the npm packages and dependencies'
        sh 'npm install'
       }
    }
    stage('Building project'){
      steps{
        echo 'Initiating npm project build'
        sh 'npm run build'
        echo 'Build has been created successfully'
      }
    }
    stage('Running tests'){
       steps{
        echo 'Running tests on to see if index.html file exists or not'
        sh 'test -f build/index.html'
       }
    }
   }
}