pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build stage'
      }
    }
    stage('Sonar') {
      steps {
        echo 'Sonar Build'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test Stage'
          }
        }
        stage('Integration') {
          steps {
            echo 'integration Test'
          }
        }
      }
    }
    stage('Release') {
      parallel {
        stage('Release') {
          steps {
            echo 'Release stage'
          }
        }
        stage('Docker') {
          steps {
            echo 'Docker image'
          }
        }
      }
    }
  }
}