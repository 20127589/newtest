pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t my-image .'
            }
        }
        stage('Push') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME')]) {
                    sh "docker login -u $USERNAME -p $PASSWORD"
                    sh 'docker push my-image'
                }
            }
        }
    }
}
