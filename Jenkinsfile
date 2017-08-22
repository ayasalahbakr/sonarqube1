 node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {

        sh "sudo docker-compose up"
    }
      stage('Push image') {
       
     
   docker.withRegistry("https://registry.hub.docker.com", 'docker-hub-credential') {

           app.push("${env.BUILD_NUMBER}")
	
	   app.push("latest") 
          
        }
    }
    stage('Deploy image') { 
	    sh "kubectl create -f deployment.yaml "
	    sh "kubectl create -f svc.yaml"
    }
}
