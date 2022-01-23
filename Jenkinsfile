pipeline {
  agent any
  stages {
    stage('build') {
      environment {
        dd = 'ee'
      }
      parallel {
        stage('build') {
          steps {
            echo 'compiling the project'
          }
        }

        stage('Test') {
          steps {
            echo 'testing the code'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the project'
      }
    }

  }
}