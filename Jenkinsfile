pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Static site - no build required'
                sh 'ls -l'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                docker rm -f portfolio-nginx || true

                docker run -d \
                  --name portfolio-nginx \
                  -p 8081:80 \
                  nginx:alpine

                docker cp . portfolio-nginx:/usr/share/nginx/html/
                '''
            }
        }
    }
}

