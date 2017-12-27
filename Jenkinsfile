pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 50000:50000'
    }
    
  }
  stages {
    stage('Checkout') {
      steps {
        sh '''
                echo \'========= Checkout stage ==========\'




                
            '''
        sh 'npm install'
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