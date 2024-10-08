pipeline {
    agent any

    tools {
      git 'Default'
      nodejs 'NodeJS 12.22.12'
    }


    stages {
      stage('Build') {
        steps {
          echo 'Building...'
          ./gradlew npm_run-script_build
        }
      }

      stage('Test') {
        steps {
          echo 'Testing...'
          ./gradlew npm_test
        }
      }

      stage('Compile') {
        steps {
          // One or more steps need to be included within the steps block.
        }
      }

      stage('Package') {
        steps {
          // One or more steps need to be included within the steps block.
        }
      }

    }

    post {
      success {
        echo 'Success'
      }
      failure {
        echo 'Failure'
      }
    }


}