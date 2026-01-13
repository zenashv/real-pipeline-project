pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Pulling code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application'
                sh 'ls -l'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application'
                sh './test.sh'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application'
                sh 'echo "Website CI pipeline executed successfully"'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline Success'
        }
        failure {
            echo 'CI pipeline Failure'
        }
    }
}
