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
        sh '''sudo apt-get install curl make -y 
curl -O https://storage.googleapis.com/golang/go1.8.linux-amd64.tar.gz
tar -xvf go1.8.linux-amd64.tar.gz
sudo mv go /usr/local'''
        echo 'make build'
        sh '''export GOROOT=/usr/local/go
export GOPATH=/tmp/Go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
mkdir -p /tmp/Go/src/github.com/sapcc/concourse-swift-resource
mv * /tmp/Go/src/github.com/sapcc/concourse-swift-resource/
cd /tmp/Go/src/github.com/sapcc/concourse-swift-resource/
go get -u github.com/FiloSottile/gvt
gvt restore
go version
make build'''
      }
    }
    stage('install docker') {
      steps {
        sh 'sudo curl -sSL https://get.docker.com/ | sh'
      }
    }
    stage('build image') {
      steps {
        sh '''


ls -alhR'''
        sh 'docker build -t richardt/con-resource .'
      }
    }
  }
}