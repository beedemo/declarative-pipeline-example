pipeline {
  agent {
    docker 'maven:3.3.3'
  }
  stages {
    stage('build') {
      steps {
        parallel(
          "build": {
            sh 'mvn --version'
            sh 'mvn install'
            
          },
          "error": {
            slackSend 'Hello'
            
          }
        )
      }
    }
  }
}