pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/Vishal-25-cyber/devops_project_1'
            }
        }

        stage('Docker Compose Test') {
            steps {
                sh 'docker-compose up --build --abort-on-container-exit'
            }
        }
    }

    post {
        always {
            sh 'docker-compose down || true'
        }
    }
}