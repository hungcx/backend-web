pipeline {
  agent { docker { image 'python:3.10-alpine' } }

  environment {
    TESTING_NAME = 'hihi'
  }

  stages {
    stage('Build') {
      steps {
        sh 'python --version'
      }
    }
    stage('Testing') {
      steps {
        echo 'Testing...${Testing}'
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
