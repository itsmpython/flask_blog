pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/itsmpython/flask_blog', branch: 'dev')
      }
    }

    stage('List Content') {
      steps {
        sh 'ls -la'
      }
    }

  }
}