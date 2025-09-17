pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'test', url: 'https://github.com/anni1007/test-repo'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example build commandjj
              // sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example test command
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to $DEPLOY_PATH ...'
                // Sample deployment (replace with your actual command)
                // sh """
                // mkdir -p $DEPLOY_PATH
                // cp -r * $DEPLOY_PATH/
               // echo 'Deployed at: ' $(date)
               // """
            }
        }
    }

    post {
        success {
            echo '✅ Build and Deployment successful.'
        }
    failure {
            echo '❌ Build or Deployment failed.'
        }
    }
}
