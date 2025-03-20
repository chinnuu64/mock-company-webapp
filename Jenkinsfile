pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/YOUR-GITHUB-USERNAME/mock-company-webapp.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}
