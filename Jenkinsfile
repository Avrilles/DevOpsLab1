pipeline {
  agent any
 
  environment {

  }
 
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
 
    stage('Build Docker images') {
      steps {
        sh 'docker-compose build'
      }
    }
 
    stage('Deploy') {
      steps {
        script {
          sh 'ssh malikova@example.com "docker-compose pull && docker-compose up -d"'
        }
      }
    }
  }
}