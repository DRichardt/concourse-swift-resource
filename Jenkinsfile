pipeline {
  agent {
    node {
      label 'Docker'
    }
    
  }
  stages {
    stage('build resource') {
      steps {
        echo 'Building concourse swift resource'
        sh 'apt-get install golang-go'
        sh 'make build'
      }
    }
  }
}