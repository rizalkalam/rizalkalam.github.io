pipeline{
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Use the 'checkout' step to pull the Git repository (if not already done)
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Any build steps needed for your HTML
                // For example, copying files to a build directory
                sh 'cp -r source_directory/* build_directory/'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                // Copy the built HTML to the Nginx directory
                sh 'sudo cp -r build_directory/* /var/www/html/'

                // Restart Nginx to apply changes
                sh 'sudo systemctl restart nginx'
            }
        }

       // stage('Deploy HTML File') {
       //      steps {
       //          // Use the 'sh' step to copy the 'index.html' file to the deployment location
       //          sh 'cp index.html /var/www/html/'
       //      }
       //  }
    }
}

