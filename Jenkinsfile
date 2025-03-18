pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ PES1UG22CS421-1.cpp -o PES1UG22CS421-1'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                sh './PES1UG22CS421-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy commands here (e.g., scp, curl, etc.)
                echo 'Deployment step completed.'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
