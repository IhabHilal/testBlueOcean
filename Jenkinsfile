pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running test2'
          }
        }

        stage('test1') {
          steps {
            echo 'Running test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Ara you sure to deploy?', ok: 'yes, i am sure')
        echo 'Deployment completed'
      }
    }

    stage('Notify for New build') {
      steps {
        echo 'New build completed'
      }
    }

  }
}