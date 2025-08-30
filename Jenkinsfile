pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git url: 'https://github.com/hodor78/selenium-docker-runner.git', branch: 'main'
      }
    }
    stage('Run Test') {
      steps { sh 'docker compose up -d' }
    }
    stage('Bring Grid Down') {
      steps { sh 'docker compose down' }
    }
  }
}
