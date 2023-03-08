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

        stage('') {
          steps {
            mail(subject: 'From Jenkins - FCC', body: 'This is a test email. Please ignore', from: 'jenkins@fcc-arjun.com', to: 'mallikarjun.somanakatti@gmail.com')
          }
        }

      }
    }

  }
}