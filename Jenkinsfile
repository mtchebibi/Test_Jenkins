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
                sh 'echo "sans erreur"'
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