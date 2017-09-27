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
        echo 'install go'
        sh 'apt-get install golang-go'
        echo 'Make build'
      }
    }
  }
}