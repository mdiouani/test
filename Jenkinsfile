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
            build 'maintainers'
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
      steps {
        echo '========= Deploy stage =========='
      }
    }
  }
}