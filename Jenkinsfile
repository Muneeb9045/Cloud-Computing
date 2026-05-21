pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // GitHub se code pull ho raha hai
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // C code ko compile karna (gcc compiler zaroori hai)
                sh 'gcc index.c -o myapp'
            }
        }
        stage('Test') {
            steps {
                // C program ko run karke test karna
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
