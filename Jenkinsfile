pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'this stage is for testing'
          }
        }

        stage('Test2') {
          steps {
            echo 'This stage is another step of testing in a react application'
          }
        }

        stage('Test3') {
          steps {
            echo 'This is the final step for testing'
          }
        }

      }
    }

    stage('Browser Test') {
      parallel {
        stage('Browser Test') {
          steps {
            echo 'Testing in Chrome'
          }
        }

        stage('Firefox') {
          steps {
            echo 'Testing in Firefox'
          }
        }

      }
    }

    stage('Dev') {
      steps {
        echo 'This stage is deliver the react application'
      }
    }

    stage('Staging') {
      steps {
        echo 'this staging the react app'
      }
    }

    stage('Production') {
      steps {
        sh 'echo $PATH '
      }
    }

  }
}