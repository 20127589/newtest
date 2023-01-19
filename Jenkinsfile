node {  
     stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
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
