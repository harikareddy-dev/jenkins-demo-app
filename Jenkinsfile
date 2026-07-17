pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking source code...'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop jenkins-demo-app || true'
                sh 'docker rm jenkins-demo-app || true'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d --name jenkins-demo-app -p 8085:80 jenkins-demo-app'
            }
        }

        stage('Deployment Complete') {
            steps {
                echo 'Application deployed successfully!'
            }
        }
    }
}