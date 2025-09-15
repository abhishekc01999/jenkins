pipeline {
    agent any
    environment {
        APP_ENV = 'dev'
        BUILD_TAG = "${env.BUILD_ID}"
    }
    stages {
        stage('Checkout') {
            steps {
                echo "📥 Pulling code (simulated)..."
            }
        }
        stage('Build') {
            steps {
                echo "🔨 Building project..."
            }
        }
        stage('Test') {
            steps {
                echo "✅ Running tests..."
            }
        }
        stage('Deploy') {
            steps {
                echo "🚀 Deploying application..."
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Environment = $APP_ENV"'
                sh 'echo "Build Tag = $BUILD_TAG"'
            }
        }
    }
}
