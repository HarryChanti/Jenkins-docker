node {   
    stage('Clone repository') {
        git credentialsId: 'git', url: 'https://github.com/HarryChanti/Jenkins-docker.git'
    }
    
    stage('Build image') {
       dockerImage = docker.build("HarryChanti/Jenkins-docker")
    }
    
 stage('Push image') {
        withDockerRegistry([ credentialsId: "dockerhubaccount", url: "" ]) {
        dockerImage.push()
        }
    }    
}
