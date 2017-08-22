 node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {

        app = docker.build("ayasalah93/voda")
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
