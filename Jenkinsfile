pipeline {
  agent {
    docker {
      label 'Docker'
      image 'richardt/jenkinscontainer'
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