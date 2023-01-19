pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/20127589/newtest.git', branch:'main'
            }
        }
        stage('Build') {
            steps {
                sh 'sudo apt-get update -y && apt-get install make -y'
                sh 'make build'
            }
        }
        stage('Test') {
            steps {
                sh 'make test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'make deploy'
            }
        }
    }
}
