pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
    
  }
  stages {
    stage('teststage') {
      steps {
        sh 'echo "test"'
      }
    }
  }
}