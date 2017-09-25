pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }
    
  }
  stages {
    stage('build docker') {
      steps {
        sh 'docker build .'
      }
    }
  }
}