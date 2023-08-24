pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build comleted'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'run test'
          }
        }

        stage('test1') {
          steps {
            echo 'run test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy completed'
      }
    }

  }
}