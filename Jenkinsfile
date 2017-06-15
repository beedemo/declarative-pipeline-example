pipeline {
  agent {
    docker 'maven:3.3.3'
  }
  stages {
    stage('Build') {
      steps {
        echo 'build'
      }
    }
    stage('Test') {
      steps {
        
        parallel(
          "integration": {
            echo 'integration tests'
          },
          "performance": {
            echo 'performance tests'
          }
        )
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
