pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t week-2'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                bat 'docker tag week-2 nuhitha216/registration:v1'
                bat 'docker push nuhitha216/registration:v1'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f C:/devops1275/week-2/deployment.yaml'
                bat 'kubectl apply -f C:/devops1275/week-2/service.yaml'
            }
        }
    }
}
