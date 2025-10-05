pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'docker build -t Docker-CI-CD .'
      }
    }
    stage('Deploy') {
      steps {
        bat 'docker run -d -p 8081:80 Docker-CI-CD'
      }
    }
  }
}
