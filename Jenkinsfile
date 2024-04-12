pipeline {    
   agent any
   triggers {
        pollSCM '* * * * *'
    }
    stages {

         stage('Checkout') {
            steps {
                echo 'OK'
                git branch: 'develop', url: 'https://github.com/fiyona2002/python-develop-branch.git'
            }
        }
        
        stage('Build') {
            steps {
                echo 'This is building stage'
            }
        }
        
        stage('Test') {
            steps {
                echo 'This is testing stage'
                bat 'python hello.py'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'This is deployment stage' 
                // Add deployment steps if applicable
            }
        }
    }
    
    post {
        always {
            // Clean up workspace
            deleteDir()
        }
        
    }
}
