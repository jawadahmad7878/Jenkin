pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main' // Replace with your branch
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build' 
            }
        }
        stage('Test') {
            steps {
                sh 'npm test' 
            }
        }
    }
}