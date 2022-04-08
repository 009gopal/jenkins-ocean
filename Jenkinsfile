pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'code tested'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'tested code build complete'
          }
        }

        stage('Build1') {
          steps {
            echo 'parallel build run'
          }
        }

      }
    }

    stage('test-deploy') {
      steps {
        echo 'deployed on test environment'
      }
    }

    stage('prod-deploy') {
      steps {
        echo 'deployed on prod environment'
      }
    }

  }
}