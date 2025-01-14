pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        script {
          // Fetch the code from the specified Git repository URL
          git branch: 'main', url: 'https://github.com/jawadahmad7878/Jenkin'
        }
      }
    }
    stage('Build') {
      steps {
        sh 'npm install' // Install project dependencies
        sh 'npm run build'  // Build the project using npm run build
      }
    }
    stage('Test') {
      steps {
        sh 'npm test' // Run unit tests using npm test
      }
    }
  }
}