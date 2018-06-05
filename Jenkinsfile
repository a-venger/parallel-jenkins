pipeline {
  agent any
  stages {
    stage('ECHO') {
      parallel {
        stage('ECHO') {
          steps {
            bat(script: 'ping 8.8.8.8', returnStdout: true, returnStatus: true)
          }
        }
        stage('ECHO2') {
          steps {
            echo 'HELLLO'
            bat(script: 'ping 9.9.9.9', returnStatus: true, returnStdout: true)
          }
        }
        stage('Ping') {
          steps {
            bat(script: 'ping 8.8.8.8', returnStdout: true)
          }
        }
        stage('ECHO3') {
          steps {
            echo 'Hello3'
          }
        }
      }
    }
  }
}