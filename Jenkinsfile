pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build comleted'
        retry(count: 2) {
          sh 'wwww'
        }

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
        input(message: 'Are you sure', ok: 'Yes')
        echo 'deploy completed'
      }
    }

    stage('Notify for new Build') {
      steps {
        echo 'New build completed successfuly'
      }
    }

  }
}