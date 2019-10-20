
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
        script {
          echo 'Stage 1'
        }
      }
    }

  stage('Build image') {
      steps{
        script {
          dockerImage = docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }  
  
  stage('Push Docker Image') {
  steps{
    script {
      docker.withRegistry( '', registryCredential ) {
        dockerImage.push()
        }
      }
    }
  }
    
    
    
  }
}
