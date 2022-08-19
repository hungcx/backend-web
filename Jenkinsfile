pipeline {
  agent none

  environment {
    TESTING_NAME = 'hihi'
  }

  stages {
    stage('Testing') {
      agent { docker { image 'python:3.10-alpine' } }
      steps {
        echo 'python --version'
      }
    }
    stage('Build') {
      agent any
      steps {
        sh 'docker build -t hihi:lastest .'
        sh 'docker image ls'
      }
    }
    stage('Deploy') {
      steps {
        echo "Deploy...${TESTING_NAME}"
      }
    }
  }

  post {
    always {
      echo 'Thanks!!!'
    }
  }
}
