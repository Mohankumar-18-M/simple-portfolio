pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Static site - no build required'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                docker exec portfolio-nginx rm -rf /usr/share/nginx/html/*
                docker cp . portfolio-nginx:/usr/share/nginx/html/
                '''
                echo 'Deployed to Nginx successfully'
            }
        }
    }
}

