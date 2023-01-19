pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
                sh 'mvn clean install'
            }
        }
        stage('Deploy') {
            steps {
                sh './deploy.sh'
            }
        }
    }
}
