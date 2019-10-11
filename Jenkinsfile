pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          args '-u 0'
          image 'alpine'
        }

      }
      steps {
        sh 'pwd; ls -la'
        sh 'apk add make gcc libc-dev libpcap-dev openssl-dev'
        sh './configure'
        sh 'make'
      }
    }
  }
}