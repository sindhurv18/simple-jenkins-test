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
                sh "kubectl apply -f deployment.yaml"
            }
        }
        
    }
}
