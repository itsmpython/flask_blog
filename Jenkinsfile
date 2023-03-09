pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/itsmpython/flask_blog', branch: 'dev')
      }
    }

    stage('List Content') {
      parallel {
        stage('List Content') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Parallel Stage Print') {
          steps {
            echo 'From within Parallel Stage'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'echo \'Docker Build Steps here\''
      }
    }

  }
}