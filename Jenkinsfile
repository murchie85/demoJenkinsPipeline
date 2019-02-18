pipeline {
  agent any
  stages {
    stage('Saye Hello') {
      steps {
        echo "Hello ${MY_NAME}!"
        sh 'java -version'
      }
    }
  }
  environment {
    MY_NAME = 'Adam'
  }
}