pipeline {
  agent any

  environment {
    IMAGE_NAME = 'week12task:latest'
  }

  stages {
    stage('Checkout Code') {
      steps {
        git branch: 'main', url: 'https://github.com/Venkiemc/emc-nodejs-app.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        bat "docker build -t %IMAGE_NAME% ."
      }
    }

    stage('Show Docker Images') {
      steps {
        bat "docker images"
      }
    }
  }
}
