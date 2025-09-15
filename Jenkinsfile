pipeline {
    agent any
    stages {
        stage('Pull Image') {
            steps {
                sh 'docker pull docker.io/library/nginx:latest'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name test-nginx nginx:latest || true'
            }
        }
        stage('Verify') {
            steps {
                sh 'curl -I http://localhost:8080'
            }
        }
    }
}

