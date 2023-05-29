pipeline {
    agent any
    
    stages {
        stage('Setup') {
            steps {
                sh 'mkdir k8s'
                sh 'cd k8s'
                sh 'git clone "https://github.com/ilove1DevOps/Jenkins-JET-A01.git"'
                sh 'minikube start'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f runpod.yaml'
                sh 'kubectl apply -f podsvc.yaml'
            }
        }
    }
}
