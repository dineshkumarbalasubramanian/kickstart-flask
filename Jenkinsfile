pipeline {
  agent {
    node {
      label 'slave'
    }

  }
  stages {
    stage('Pre-Build') {
      steps {
        sh 'echo \'Test prebuild\''
      }
    }

    stage('Build') {
      parallel {
        stage('Build/Linux') {
          steps {
            sh 'echo \'Build Script on Linux\''
          }
        }

        stage('Build/Windows') {
          steps {
            sh 'echo \'Build script on Windows\''
          }
        }

        stage('Build/Mac') {
          steps {
            sh 'echo \'Build script on mac\''
          }
        }

      }
    }

  }
  environment {
    ENV = 'QA'
  }
}