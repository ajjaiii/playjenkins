
pipeline {
  
  environment {
    registry = "ajjaiii/myweb"
    registryCredential = 'dockerhub'
  }
  
  agent any
  stages {

    stage('Checkout update repo') {
      steps {
        git 'https://github.com/justmeandopensource/playjenkins.git'
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
    
  stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "myweb.yaml", credentialsType: "SSH")
        }
      }
    }  
    
  }
}
