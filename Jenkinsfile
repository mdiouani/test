pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh '''stages {
        stage(\'Checkout\') {
            steps {
                echo \'========= Checkout stage ==========\'




                
            }
        }'''
        }
      }
      stage('Message') {
        steps {
          sh '''echo \'Do you wish to install this program?\'



















'''
        }
      }
      stage('Choice') {
        agent any
        steps {
          sh 'ping -c 3 localhost'
        }
      }
      stage('error') {
        steps {
          sh '''echo \'Do you wish to install this program?\'
select yn in "Yes" "No"; do
    case $yn in
        Yes ) make echo \'install\'; break;;
        No ) echo \'no install\';;
    esac
done'''
        }
      }
    }
  }