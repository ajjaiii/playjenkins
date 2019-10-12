pipeline {
    agent any
    stages {
        stage('Checkout Source') {
            steps {
                   sh "sudo apt update"
                   sh "sudo apt install git"
                   git url: 'https://github.com/ajjaiii/playjenkins.git', branch: 'master'
            }
        }
     }
}
