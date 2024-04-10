pipeline {
  agent any
  properties([[$class: 'JiraProjectProperty'], disableConcurrentBuilds(), parameters([string(defaultValue: '111', name: 'test', trim: true)]), pipelineTriggers([cron('0 2 * * *')])])
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
