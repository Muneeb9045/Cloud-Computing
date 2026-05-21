pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Notify') {
            steps {
                echo 'Success!'
            }
        }
    }
}
