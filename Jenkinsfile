pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/Ajayvarma8142/eShopOnWeb.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        sh 'dotnet build eShopOnWeb.sln'
      }
    }
    
 stage('Nunit Test') {
      parallel {
        stage('Integration Test') {
          steps {
            echo 'Tests'
          }
        }
        /*stage('Junit') {
          steps {
            echo 'junit tests'
            sh 'mvn test -B -Dmaven.javadoc.skip=true -Dcheckstyle.skip=true'
          }
        }*/
        stage('code coverage') {
          steps {
            echo 'code coverage test cases'
          }
        }
        stage('Dev') {
      steps {
        echo 'Dev env'
      }
    }
        stage('QA Test') {
      steps {
        echo 'QA env'
      }
    }
    stage('LT') {
      steps {
        echo 'LT env'
      }
    }
    stage('UAT') {
      steps {
        echo 'UAT env'
      }
    }
  }

