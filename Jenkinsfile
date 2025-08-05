pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t my-app .'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                sh 'node app-test.js'  // 
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploy step ( docker run or copy to server)"'
            }
        }
    }
}
