pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh '''pwd
ls'''
            timeout(time: 1) {
              echo 'test'
            }

          }
        }

        stage('') {
          steps {
            timestamps() {
              sh 'echo 1111'
              sleep 2
              sh 'echo 222'
            }

          }
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