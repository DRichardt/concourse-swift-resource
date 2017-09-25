pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
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