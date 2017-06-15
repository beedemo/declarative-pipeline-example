pipeline {
  agent {
    docker 'maven:3.3.3'
  }
  stages {
    stage('Build') {
      steps {
        parallel(
          "build": {
            sh 'mvn --version'
            sh 'mvn install'
          },
          "error": {
            slackSend 'build error'
          }
        )
      }
    }
    stage('Test') {
      steps {
        echo 'test'
      }
    }
    stage('Package') {
      steps {
        echo 'package'
      }
    }
    stage('Release') {
      steps {
        echo 'release'
      }
    }
    stage('Configure') {
      steps {
        echo 'configure'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
}
