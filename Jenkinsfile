pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        script {
          git branch: 'main', url: 'https://github.com/jawadahmad7878/Jenkin'
        }
      }
    }
    stage('Build') {
      steps {
        sh 'sh build.sh' 
      }
    }
    stage('Test') {
      steps {
        sh 'sh test.sh' 
      }
    }
    stage('Build Docker Image') {
      steps {
        docker.build(imageName: 'your_image_name:latest', Dockerfile: 'Dockerfile') 
      }
    }
  }
}