pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'docker run --rm devops-app npm test'
            }
        }
    }
}