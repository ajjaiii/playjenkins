
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
        sh 'docker version'
        script {
          echo 'Stage 1'
        }
      }
    }

    
    
  }
}
