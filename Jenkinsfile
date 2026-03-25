pipeline {
    agent any

    stages {
        stage('Docker Compose Test') {
            steps {
                sh 'docker compose up --build --abort-on-container-exit'
            }
        }
    }

    post {
        always {
            sh 'docker compose down || true'
        }
    }
}