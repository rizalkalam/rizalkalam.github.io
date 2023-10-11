pipeline{
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Use the 'checkout' step to pull the Git repository (if not already done)
                checkout scm
            }
        }

       stage('Deploy HTML File') {
            steps {
                // Use the 'sh' step to copy the 'index.html' file to the deployment location
                sh 'cp index.html /var/www/html/'
            }
        }
    }
}

