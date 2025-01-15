pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        script {
          git branch: 'main', url: 'https://github.com/jawadahmad7878/Jenkin'  // Replace with your actual Git repository URL
        }
      }
    }
    stage('Build') {
      steps {
        sh 'sh build.sh'  // Execute your build script
      }
    }
    stage('Test') {
      steps {  # Add test commands here if needed
        // sh 'sh test.sh'  # Uncomment if you have a test script (test.sh)
      }
    }
    stage('Build Docker Image') {
      steps {
        script {
          docker.build(imageName: 'your_image_name:latest', Dockerfile: 'Dockerfile')  // Replace 'your_image_name:latest' with your desired image name and tag
        }
      }
    }
    stage('Run Locally (Optional)') {
      steps {
        script {
          docker run -it --rm your_image_name:latest  # Replace with your image name
        }
      }
    }
  }
}