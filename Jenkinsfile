pipeline {
    agent any

    environment {
        // Define environment variables here if needed
        NODE_ENV = 'production'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                // Checkout the code from your Git repository
                git 'https://github.com/your-repository.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                // Install npm dependencies
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the React application...'
                // Build the React application
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run tests
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Deploy the application
                // Add deployment steps here, for example:
                // sh './deploy.sh'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Actions to perform after the pipeline completes, like cleaning up workspace
            cleanWs()
        }
    }
}
