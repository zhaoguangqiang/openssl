pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'building....'
            bat(script: 'python', returnStatus: true, returnStdout: true)
            sleep 10
          }
        }
        stage('Build1') {
          steps {
            echo 'build another file'
            sleep 10
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