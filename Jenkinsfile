pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build stage'
        sleep 30
      }
    }
    stage('Sonar') {
      steps {
        echo 'Sonar Build'
        sleep 30
      }
    }
    stage('Testing') {
      parallel {
        stage('Unit') {
          steps {
            echo 'Test Stage'
            sleep 30
          }
        }
        stage('Integration') {
          steps {
            echo 'integration Test'
            sleep 20
          }
        }
      }
    }
    stage('Release') {
      parallel {
        stage('Release') {
          steps {
            echo 'Release stage'
            sleep 10
          }
        }
        stage('Docker') {
          steps {
            echo 'Docker image'
            sleep 20
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