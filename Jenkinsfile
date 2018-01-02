pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh '''
                echo \'========= Checkout stage ==========\'




                
            '''
      }
    }
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh ' echo \'========= Build stage ==========\''
          }
        }
        stage('Maintainers') {
          steps {
            input '"Proceed"'
          }
        }
      }
    }
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        input 'Finished using the web site ? (Click "proceed" to continue'
      }
    }
    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo '========= Deploy stage =========='
          }
        }
        stage('send a mail') {
          steps {
            mail(body: 'This will go into the body of the mail.', subject: 'Test mail in blue ocean pipeline', from: 'diouani.malik@gmail.com', to: 'diouani.malik@gmail.com')
          }
        }
      }
    }
  }
}