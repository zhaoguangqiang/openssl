pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'building....'
            bat(script: 'python', returnStatus: true, returnStdout: true)
          }
        }
        stage('Build1') {
          steps {
            echo 'build another file'
          }
        }
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