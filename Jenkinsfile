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
        sh '''export GOPATH=/root/Go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
mkdir -p /root/Go/src/github.com/sapcc/concourse-swift-resource
sudo mv * /root/Go/src/github.com/sapcc/concourse-swift-resource/
sudo cd /root/Go/src/github.com/sapcc/concourse-swift-resource/
sudo make build'''
      }
    }
  }
}