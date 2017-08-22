 node {
    def app

    stage('Deploy image') { 
	    sh "kubectl get pods "
	    sh "kubectl create -f deployment.yaml"
	    sh "kubectl create -f svc.yaml"
	    sh "kubectl get pods "
    }
}
