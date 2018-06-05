pipeline {
  agent any
  stages {
    stage('ECHO') {
      parallel {
        stage('PING1') {
          steps {
            bat(script: 'ping 8.8.8.8', returnStdout: true, returnStatus: true)
            bat(script: 'ping 9.9.9.9', returnStatus: true, returnStdout: true)
            bat(script: 'ping 10.10.10.10', returnStatus: true, returnStdout: true)
          }
        }
        stage('PING2') {
          steps {
            echo 'HELLLO'
            bat(script: 'ping 9.9.9.9', returnStatus: true, returnStdout: true)
            bat(script: 'ping 7.7.7.7', returnStatus: true, returnStdout: true)
            bat 'ping 8.8.8.8'
          }
        }
        stage('Ping 3') {
          steps {
            bat(script: 'ping 8.8.8.8', returnStdout: true)
            bat 'ping 9.9.9.9'
            bat 'ping 6.6.6.6'
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