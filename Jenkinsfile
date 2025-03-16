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
                sh 'pwd && ls -l'  // Debugging step
                sh 'g++ hello.cpp -o output'  // Compile C++ program
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './output'  // Run compiled program
                echo 'Test Stage Successful'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
