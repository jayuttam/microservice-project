pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/jayuttam/microservice-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t microservice-image .'
            }
        }

        stage('Deploy Kubernetes Pod') {
            steps {
                bat 'kubectl apply -f pod.yaml'
            }
        }
    }
}