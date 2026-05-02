pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Pulling source code'
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image'
                sh 'docker build -t devops-app:latest .'
            }
        }

        stage('List Images') {
            steps {
                sh 'docker images'
            }
        }

    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }

        failure {
            echo 'Pipeline failed'
        }
    }
}
