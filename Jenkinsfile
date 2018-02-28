pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'building....'
            bat(script: 'python test.py ${buildParam}', returnStatus: true, returnStdout: true)
            sleep 10
          }
        }
        stage('Build1') {
          steps {
            echo 'build another file'
            sleep 10
            bat(script: 'python test.py ${buildParam}', returnStatus: true)
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
  environment {
    buildParam = 'buildParam1'
    build1Param = 'buildParam2'
  }
}