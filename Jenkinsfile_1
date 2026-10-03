pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from repository...'
                // In a real setup, this is where it clones your GitHub repo
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Compiling code or installing dependencies happens here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
                // Running unit tests happens here
                sh 'echo "Simulating tests..." && exit 0'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application to production...'
                // Moving code to a server happens here
            }
        }
    }
}
