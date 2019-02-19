pipeline {
  agent any
  stages {
    stage('Print') {
      steps {
        echo "Hello ${params.Name}!"
        sh 'java -version'
      }
    }
    stage('Version Check') {
      options {
        timeout(time: 30, unit: 'SECONDS')
      }
      input {
        message 'Which Version?'
        id 'Deploy'
        parameters {
          choice(name: 'APP_VERSION', choices: '''v1.1
v1.2
v1.3''', description: 'What to deploy?')
        }
      }
      steps {
        echo "Deploying ${APP_VERSION}."
      }
    }
    stage('Deploy') {
         steps {
            echo 'Deploying....'
         }
      }



  }
  environment {
    MY_NAME = 'Adam'
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'

    }

  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}