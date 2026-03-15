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
        sh "docker build -t $IMAGE_NAME ."
      }
    }

    stage('Show Docker Images') {
      steps {
        sh "docker images"
      }
    }
  }
}
