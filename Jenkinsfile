pipeline {
  agent any

  environment {
    APP_NAME = "my-app"
  }

  stages {
    stage('Clone') {
      steps {
    	git branch: 'main', url: 'https://github.com/hashemshibli/ci-cd-app.git'
      }
    }

    stage('Build') {
      steps {
        echo 'Building the application...'
        sh 'echo Build complete'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'echo All tests passed'
      }
    }

    stage('Deploy to Test') {
      steps {
        echo 'Deploying to test environment...'

        sh 'echo Deploy to test complete'
      }
    }

    stage('Approval') {
      steps {
        input message: 'Deploy to production?', ok: 'Approve'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Deploying to production environment...'
        sh 'echo Production deployment complete'
      }
    }
  }
}

