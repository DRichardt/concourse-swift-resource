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
        sh '''export GOPATH=/tmp/Go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
mkdir -p /tmp/Go/src/github.com/sapcc/concourse-swift-resource
mv * /tmp/Go/src/github.com/sapcc/concourse-swift-resource/
cd /tmp/Go/src/github.com/sapcc/concourse-swift-resource/
go get -u github.com/kardianos/govendor
govendor fetch
make build'''
      }
    }
  }
}