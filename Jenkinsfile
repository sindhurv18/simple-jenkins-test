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

                sh """
                 kubectl get namespaces
                 kubectl apply -f deployment.yaml -n devl-srv
                """
            }
        }

        stage ("Check Deployment") {
            steps {

                sh 'kubectl get deploy -n devl-srv'
            }
        }
        stage ("Delete Deployment") {
            steps {

                sh 'kubectl delete deploy nginx-deployment -n devl-srv'
            }
        }
    }
}
