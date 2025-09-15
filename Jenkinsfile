pipeline {
    agent any
    stages {
        stage('Build Docker') {
            steps {
                sh 'docker build -t myapp:latest .'
            }
        }
        stage('Run Docker') {
            steps {
                sh 'docker run -d -p 8081:8080 --name myapp myapp:latest || true'
            }
        }
    }
}

