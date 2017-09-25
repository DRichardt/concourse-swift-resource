pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
    
  }
  stages {
    stage('install docker') {
      steps {
        sh 'docker version'
      }
    }
  }
}