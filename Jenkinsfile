
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code retrieved from GitHub'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls -la'
                sh 'test -f index.html'
                echo 'HTML file exists!'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the web application...'
                echo 'Build completed successfully!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
