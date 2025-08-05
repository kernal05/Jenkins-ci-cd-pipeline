pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Starting the application...'
                // Stop any existing app running on port 3000
                sh 'pkill -f "node app.js" || true'  
                // Start the app in background (you can use pm2 or nohup in real scenario)
                sh 'nohup npm start &'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
