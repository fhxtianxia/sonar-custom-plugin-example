pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls'''
        timeout(time: 1) {
          echo 'test'
        }

      }
    }

    stage('scan') {
      steps {
        sleep 2
      }
    }

  }
}