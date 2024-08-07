pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build commands here
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test commands here
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy commands here
            }
        }
    }

    post {
        always {
            mail (
                to: 'ranjanshruti186@gmail.com'
                subject: "Build ${currentBulid.fullDisplayName} completed",
                body: "Build ${currentBulid.fullDisplayName} completed. Check Console output at $(env.BUILD_URL}"
              )
        }
    }
}
