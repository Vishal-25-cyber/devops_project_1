pipeline {
    agent {
        docker {
            image 'docker:20.10.17'
            args '-v /var/run/docker.sock:/var/run/docker.sock -v /usr/bin/docker:/usr/bin/docker'
        }
    }

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