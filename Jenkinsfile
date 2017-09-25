pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
    
  }
  stages {
    stage('install docker') {
      steps {
        sh '''apt-get update
apt install docker.io'''
      }
    }
    stage('build concourse-swift') {
      steps {
        sh 'docker build .'
      }
    }
  }
}