pipeline {
  agent any
  stages {
    stage('ECHO') {
      parallel {
        stage('ECHO') {
          steps {
            bat(script: 'echo hello1', returnStdout: true)
          }
        }
        stage('ECHO2') {
          steps {
            echo 'HELLLO'
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