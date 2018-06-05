pipeline {
  agent any
  stages {
    stage('Parallel') {
      parallel {
        stage('PING1') {
          steps {
            bat 'ping 8.8.8.8'
            bat 'ping 9.9.9.9'
            bat 'ping google.com'
          }
        }
        stage('PING2') {
          steps {
            echo 'HELLLO'
            bat 'ping 9.9.9.9'
            bat 'ping google.com'
            bat 'ping 8.8.8.8'
          }
        }
        stage('Ping 3') {
          steps {
            bat 'ping 8.8.8.8'
            bat 'ping 9.9.9.9'
            bat 'ping google.com'
          }
        }
        stage('ECHO3') {
          steps {
            echo 'Hello3'
          }
        }
      }
    }
    stage('Build initiation') {
      steps {
        powershell '$users = 100; $nodes = 3; $users_per_node = [Math]::Ceiling($users/$nodes); Write-Host $users_per_node'
      }
    }
  }
}