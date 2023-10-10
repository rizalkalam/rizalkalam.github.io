pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                // Copy your application to the web server directory
                sh 'rsync -avz --exclude=".env" . /var/www/html'
                // Restart the web server (e.g., Nginx)
                sh 'systemctl restart nginx'
            }
        }

        // Add more stages for building, testing, and deploying your project
    }
}
