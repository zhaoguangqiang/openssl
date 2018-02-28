pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'building....'
        bat(script: 'python', returnStatus: true, returnStdout: true)
      }
    }
    stage('Test') {
      steps {
        echo 'testing....'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploying....'
      }
    }
  }
}