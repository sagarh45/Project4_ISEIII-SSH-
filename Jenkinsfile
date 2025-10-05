pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t ise-ci-app .'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker run -d -p 8081:80 ise-ci-app'
      }
    }
  }
}
