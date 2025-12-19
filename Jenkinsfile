pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/<your-username>/simple-portfolio.git'
            }
        }

        stage('Build') {
            steps {
                echo "No build needed for static site"
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                mkdir -p /tmp/portfolio
                cp index.html /tmp/portfolio/
                '''
            }
        }
    }
}
