pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Compilation en cours..."'
            }
        }
        stage('Test en échec') {
            steps {
                sh 'exit 1'
            }
        }
    }

    post {
        success {
            echo 'Pipeline réussi'
        }
        failure {
            echo 'Pipeline en échec'
        }
    }
}