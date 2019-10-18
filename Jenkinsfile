
pipeline {
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

    stage('Stage 2') {
      steps {
        script {
          echo 'Stage 2'
          sh 'usermod -aG docker jenkins'
          sh 'docker version'
        }
      }
    }

  }
}
