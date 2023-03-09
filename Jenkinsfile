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

    stage('Login to Dockerhub') {
      environment {
        DOCKERHUB_USERNAME = 'username'
        DOCKERHUB_PASSWORD = 'password'
      }
      steps {
        sh '''echo \'This step logs the system into Dockerhub or any of your destination server\'
echo \'Docker login command --> docker login -u $DOCKERHUB_USERNAME -p DOCKERHUB_PASSWORD\'
echo \'Refer to the $DOCKERHUB_USERNAME & $DOCKERHUB_PASSWORD env variables in settings\''''
      }
    }

    stage('Push/Deploy to Dockerhub') {
      steps {
        sh '''echo \'This step deploys the image to docker container\'
echo \'Docker command is --> docker push username/github-folder:latest\'
'''
      }
    }

  }
}
