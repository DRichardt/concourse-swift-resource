pipeline {
  agent {
    docker {
      image 'evarga/jenkins-slave'
    }
    
  }
  stages {
    stage('install docker') {
      steps {
        sh 'echo "test"'
      }
    }
  }
}