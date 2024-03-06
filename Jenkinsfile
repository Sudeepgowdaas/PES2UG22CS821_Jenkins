pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed.'
        }
    }
}
