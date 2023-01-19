node {   
    stage('Clone repository') {
        git credentialsId: 'git', url: 'https://github.com/20127589/newtest.git'
    }
    
    stage('Build image') {
       dockerImage = docker.build("2imfatx/20127589:latest")
    }
    
 stage('Push image') {
        withDockerRegistry([ credentialsId: "dockerhub", url: "" ]) {
        dockerImage.push()
        }
    }    
}
