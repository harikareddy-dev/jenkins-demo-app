pipeline {
    agent any

    stages {
<<<<<<< HEAD
=======

>>>>>>> b8d2904ab9f036d4910e94c6dba1d4127076383b
        stage('Checkout') {
            steps {
                echo 'Checking source code...'
            }
        }

<<<<<<< HEAD
        stage('Build') {
            steps {
                echo 'Building Docker Image...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
=======
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
>>>>>>> b8d2904ab9f036d4910e94c6dba1d4127076383b
            }
        }
    }
}