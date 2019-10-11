pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          image 'alpine'
        }

      }
      steps {
        sh 'pwd; ls -la'
        sh './configure'
      }
    }
  }
}