pipeline {
    agent any

    stages {
        stage('Start') {
            steps {
                echo "=== Start pipeline ==="
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
            }
        }
    }

    post {
        always {
            echo "Pipeline finished."
        }
    }
}
