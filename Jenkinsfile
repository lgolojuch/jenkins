pipeline {
    agent any

    stages {
        stage('Start') {
            steps {
                echo "=== Start pipeline ==="
            }
        }

        stage('Checkout') {
            steps {
                echo "Checkout to the repo..."
                git url: 'https://github.com/lukaszgolojuch/PlaywrightTests', branch: "main"
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh './gradlew clean test'
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
