pipeline {
    agent any
    stages {
        stage ("list file") {
            steps{
                sh "ls -lr"
            }
            
        }
        stage ("Deployment") {
            steps {

                sh "kubectl get namespaces"
                
                sh "kubectl apply -f deployment.yaml -n devl-srv"
            }
        }

        stage ("Check Deployment") {
            steps {

                sh 'kubectl get deploy -n devl-srv'
            }
        }
        
    }
}
