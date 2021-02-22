pipeline {
  agent {
    docker 'node:7.10-alpine'
  }
  stages {
    stage('Build') {
      agent {
        label k8
      }
      steps {
        echo 'Building..'
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
        sh 'npm t'
      }
    }
  }
}
