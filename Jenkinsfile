pipeline {
    agent any

    environment {
        APP_NAME = "my-demo-app"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/datng-dev/vault-spring.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building ${APP_NAME}..."
                sh 'echo "Simulating build process"'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                sh 'echo "Deployed successfully!"'
            }
        }
    }

    post {
        success {
            echo "Pipeline finished successfully 🎉"
        }
        failure {
            echo "Pipeline failed ❌"
        }
    }
}
