pipeline {
  agent {
    docker {
      image 'ubuntu'
    }
    
  }
  stages {
    stage('install docker') {
      steps {
        sh 'echo "test"'
      }
    }
  }
  environment {
    http_proxy = 'proxy.wdf.sap.corp:8080'
    https_proxy = 'proxy.wdf.sap.corp:8080'
    no_proxy = '127.0.0.1, localhost, *.sap.com, *.sap.corp, *cloud.sap, *sap*, .cloud.sap, moo-repo.wdf.sap.corp'
  }
}