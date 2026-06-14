pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t cicd-app:latest .'
            }
        }

        stage('Load Image To Minikube') {
            steps {
                bat 'minikube image load cicd-app:latest'
            }
        }

        stage('Deploy To Kubernetes') {
            steps {
                bat 'kubectl apply -f deployment.yaml'
                bat 'kubectl apply -f service.yaml'
            }
        }

        stage('Rolling Update') {
            steps {
                bat 'kubectl rollout restart deployment cicd-app'
            }
        }

        stage('Verify Deployment') {
            steps {
                bat 'kubectl get pods'
            }
        }
    }
}
