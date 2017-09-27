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
        sh 'sudo apt-get -y install golang-go make'
        echo 'make build'
        sh '''export GOPATH=$(HOME)/Go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
mkdir -p $(HOME)/Go/src/github.com/sapcc/concourse-swift-resource
mv * $(HOME)/Go/src/github.com/sapcc/concourse-swift-resource/
cd $(HOME)/Go/src/github.com/sapcc/concourse-swift-resource/
make build'''
      }
    }
  }
}