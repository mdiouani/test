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
      steps {
        sh 'echo \'test\''
      }
    }
    stage('Deploy') {
      steps {
        echo '========= Deploy stage =========='
      }
    }
  }
}