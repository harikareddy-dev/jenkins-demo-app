pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking source code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker Image...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
}