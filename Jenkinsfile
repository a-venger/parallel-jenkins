pipeline {
  agent any
  stages {
    stage('ECHO') {
      parallel {
        stage('PING1') {
          steps {
            bat 'ping 8.8.8.8'
            bat 'ping 9.9.9.9'
            bat 'ping 10.10.10.10'
          }
        }
        stage('PING2') {
          steps {
            echo 'HELLLO'
            bat 'ping 9.9.9.9'
            bat 'ping 7.7.7.7'
            bat 'ping 8.8.8.8'
          }
        }
        stage('Ping 3') {
          steps {
            bat 'ping 8.8.8.8'
            bat 'ping 9.9.9.9'
            bat 'ping 10.10.10.10'
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