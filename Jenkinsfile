pipeline {
  agent {
    docker {
      image 'evarga/jenkins-slave'
      label 'Docker'
    }
    
  }
  stages {
    stage('Teststage') {
      steps {
        sh 'echo "test"'
      }
    }
  }
}
