pipeline {
  agent {
    node {
      label 'npm'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

  }
}