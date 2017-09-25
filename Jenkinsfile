pipeline {
  agent any
  stages {
    stage('install docker') {
      steps {
        sh 'docker build .'
      }
    }
  }
}