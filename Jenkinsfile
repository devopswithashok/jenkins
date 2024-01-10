pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                // Install Node.js and npm
                // This assumes you have Node.js and npm installed on your Jenkins agent
                sh 'sudo npm install'
            }
        }

        stage('Build') {
            steps {
                // Build the Angular application
                sh 'sudo npm run build'
            }
        }

        stage('Test') {
            steps {
                // Run tests if applicable
                sh 'sudo npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your Angular application (e.g., copy files to a web server)
                // You may need additional steps based on your deployment strategy
                // For example, you can use rsync, scp, or other methods to copy files
                sh 'rsync -avz --delete dist/ your-server:/path/to/deploy'
            }
        }
    }

    post {
        success {
            // You can add post-build actions here
            echo 'Build and deployment successful!'
        }

        failure {
            // You can add actions to be executed if the build fails
            echo 'Build or deployment failed!'
        }
    }
}
