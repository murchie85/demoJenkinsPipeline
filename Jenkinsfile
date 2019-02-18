pipeline {
  agent any
  stages {
    stage('Saye Hello') {
      steps {
        echo "Hello ${MY_NAME}!"
        sh 'java -version'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
  }
  environment {
    MY_NAME = 'Adam'
    TEST_USER = credentials('test-user')
  }
}