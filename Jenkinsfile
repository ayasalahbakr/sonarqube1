 node {
    def app
	 
    stage('pre-request') {
        sh "curl -LO https://storage.googleapis.com/kubernetes-release/release/\$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
	sh "chmod +x ./kubectl"
	sh "sudo mv ./kubectl /usr/local/bin/kubectl"
    }
    stage('Deploy image') { 
	    sh "kubectl get pods "
	    
    }
}
