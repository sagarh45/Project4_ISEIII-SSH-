pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'docker build -t ise-ci-app .'
      }
    }
    stage('Deploy') {
      steps {
        bat 'docker run -d -p 8081:80 ise-ci-app'
      }
    }
  }
}
