
pipeline {
  
  environment {
    registry = "ajjaiii/myweb"
    registryCredential = 'dockerhub'
  }
  
  agent any
  stages {

    stage('Checkout repo') {
      steps {
        git 'https://github.com/justmeandopensource/playjenkins.git'
        sh 'whoami'
        sh 'ls -al /var/run/'
        script {
          echo 'Stage 1'
        }
      }
    }

    
    
  }
}
