pipeline {
    agent any
    stages {
        stage ("list file") {
            sh "ls -lr"
        }

        stage ("Deployment") {
            sh "kubectl apply -f deployment.yaml"
        }
        
    }
}
