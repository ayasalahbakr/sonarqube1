 node {
    def app
	 
    stage('Clone repository') {
        checkout scm
    }

    stage('Deploy image') { 
	    sh "kubectl delete -f deployment1.yaml"
	    sh "kubectl create -f svc1.yaml"
	    sh "kubectl get pods "
	    sh "kubectl create -f deployment1.yaml"
	    sh "kubectl create -f svc1.yaml"
	    sh "kubectl get pods "
    }
}
