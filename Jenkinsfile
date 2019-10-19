
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
        sh 'systemctl start docker'
        sh 'systemctl enable docker' 
        sh 'ls -al /var/run/docker.sock'
        script {
          echo 'Stage 1'
        }
      }
    }

    
    
  }
}
