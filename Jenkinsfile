pipeline {
  agent {
    node { label 'k8' }
    docker {
       image 'node:7.10-alpine'
       label 'k8'
    }
  }
  stages {
    stage('Build') {
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
