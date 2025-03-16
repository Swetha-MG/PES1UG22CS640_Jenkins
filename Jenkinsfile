pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o output'  // Update filename here
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './output'
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
