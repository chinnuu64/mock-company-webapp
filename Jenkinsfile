pipeline {
    agent any  // Runs on any available agent

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm  // Gets the latest code
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh './gradlew assemble'  // Runs Gradle build command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './gradlew test'  // Runs tests
            }
        }
    }

    post {
        success {
            echo '✅ Build and tests passed successfully!'
        }
        failure {
            echo '❌ Build or tests failed. Please check logs.'
        }
    }
}
