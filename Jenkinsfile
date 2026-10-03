pipeline {
    agent {
        // This launches a lightweight Python Docker container to run your code
        docker { image 'python:3.10-slim' } 
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Lint / Code Quality') {
            steps {
                echo 'Checking syntax...'
                sh 'python3 -m py_compile app.py'
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Executing Python tests...'
                sh 'python3 app.py'
            }
        }
        stage('Deploy Sandbox') {
            steps {
                echo 'Simulating deployment...'
                sh 'echo "App successfully verified and packaged!"'
            }
        }
    }
}
