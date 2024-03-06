pipeline {
    agent any

    stages {
        stage('Build') {
    steps {
            sh 'invalid_command'
        }
    }

        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed.'
        }
    }
}
