pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code already checked out by Jenkins'
                sh 'ls -la'
            }
        }

        stage('Build') {
            steps {
                echo 'Building portfolio'
            }
        }

        stage('Test') {
            steps {
                echo 'No tests for static site'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment successful'
            }
        }
    }
}

