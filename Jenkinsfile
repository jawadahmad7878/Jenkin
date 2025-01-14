pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                    git branch: 'main' url: 'https://github.com/jawadahmad7878/Jenkin' } // Replace with your details

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