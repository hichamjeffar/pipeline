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
    stage('Testing') {
      parallel {
        stage('Unit') {
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
    stage('Deploy') {
      parallel {
        stage('Server Int 1') {
          steps {
            echo 'Deploy to Server 1'
          }
        }
        stage('Server Int 2') {
          steps {
            echo 'Deploy to server 2'
          }
        }
        stage('Server Int 3') {
          steps {
            echo 'Deploy to server 3'
          }
        }
      }
    }
    stage('Selunium') {
      parallel {
        stage('Desktop') {
          steps {
            echo 'testing Desktop'
          }
        }
        stage('Ipad') {
          steps {
            echo 'Testing Ipad'
          }
        }
        stage('Surface') {
          steps {
            echo 'Testing Surface'
          }
        }
      }
    }
  }
}