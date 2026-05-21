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
                // Hum 'sh' ki bajaye direct command chala kar check karte hain
                sh 'echo "Installing GCC..."'
                // Jenkins container mein hum root nahi hain, isliye sh se install mushkil hai.
                // Lekin hum gcc ki jagah check karte hain k kya yahan 'clang' ya 'gcc' path mein hai?
                sh 'gcc --version || echo "GCC not found, please check agent environment"'
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
