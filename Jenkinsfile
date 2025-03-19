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
        echo 'Deployment completed'
      }
    }

  }
}