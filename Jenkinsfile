pipeline {
    agent any

    parameters {
        string(name: 'BRANCH', defaultValue: 'main', description: 'Checkout branch')
    }
    
    stages {
        stage('Start') {
            steps {
                echo "=== Start pipeline ==="
            }
        }

        stage('Checkout') {
            steps {
                echo "Checkout to the repo..."
                git url: 'https://github.com/lukaszgolojuch/PlaywrightTests', branch: "$params.BRANCH"
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
