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
      steps {
        sh ' echo \'========= Build stage ==========\''
      }
    }
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh './jenkins/test.sh'
      }
    }
    stage('Deploy') {
      steps {
        echo '========= Deploy stage =========='
      }
    }
  }
}