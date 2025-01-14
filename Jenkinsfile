pipeline {
  agent any

tools {
    bash 'my-bash' {
      path '/c/Program Files/Git/bin/bash.exe' 
    }
  }
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
        // Assuming your build commands are in a shell script named build.sh
        sh 'sh build.sh'  // Execute the build script
      }
    }
    stage('Test') {
      steps {
        // Assuming your test commands are in a shell script named test.sh
        sh 'sh test.sh'  // Execute the test script
      }
    }
  }
}