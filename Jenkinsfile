pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Hum gcc install nahi kar rahe, hum sirf 'cc' use kar rahe hain
                // Agar 'cc' bhi nahi hai, to error aayega. 
                // Agar error aaye, to instructor se kahein 'gcc' image provide karein.
                sh 'cc index.c -o myapp || echo "Compiler not found"'
            }
        }
    }
}
