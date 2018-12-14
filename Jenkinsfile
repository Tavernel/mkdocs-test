pipeline {
  agent {
    docker {
      image 'squidfunk/mkdocs-material'
      args '-v $WORKSPACE:/docs --entrypoint bash'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''mkdocs build
ls -l _site'''
      }
    }
    stage('Test') {
      steps {
        sh 'ls -l'
      }
    }
  }
}