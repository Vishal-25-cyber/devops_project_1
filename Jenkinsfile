pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'sudo docker build -t devops-app .'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'sudo docker run --rm devops-app npm test'
            }
        }
    }
}