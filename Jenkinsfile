pipeline {
    agent any

    environment {
        EMAIL_RECIPIENT = 'myrahulsaini1998@gmail.com'  // Change to your email
    }

    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                // Use full path for pip3
                sh '/usr/bin/pip3 install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest tests/'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to staging...'
                // Example deploy command (modify as needed):
                sh 'echo Deployment step - customize this for your staging environment'
            }
        }
    }

    post {
        success {
            mail to: "${env.EMAIL_RECIPIENT}",
                 subject: "Build Success: ${env.JOB_NAME} - Build #${env.BUILD_NUMBER}",
                 body: "Jenkins build passed successfully."
        }
        failure {
            mail to: "${env.EMAIL_RECIPIENT}",
                 subject: "Build Failed: ${env.JOB_NAME} - Build #${env.BUILD_NUMBER}",
                 body: "Jenkins build failed. Please check the logs."
        }
    }
}
