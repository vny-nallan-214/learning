pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git
                checkout scm
            }
        }
        
        stage('Setup Python') {
            steps {
                script {
                    // Example: Set up a Python environment
                    sh 'python3 -m venv venv'
                    sh './venv/bin/pip install -r requirements.txt'  // if you have dependencies
                }
            }
        }
        
        stage('Run Tests') {
            steps {
                script {
                    // Run tests (example with pytest for Python)
                    sh './venv/bin/python -m pytest'
                }
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add build steps if needed
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // Deploy steps go here
            }
        }
    }
}

