pipeline {
    agent {
        docker {
            image 'gcc:latest'
            // Yeh container ko root privileges dega taake build ho sake
            args '-u root'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'gcc index.c -o myapp'
            }
        }
        stage('Test') {
            steps {
                sh './myapp'
            }
        }
        stage('Notify') {
            steps {
                echo 'Pipeline completed successfully!'
            }
        }
    }
}
