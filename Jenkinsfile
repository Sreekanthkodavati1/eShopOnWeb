pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/Sreekanthkodavati1/eShopOnWeb.git', branch: 'master', credentialsId: 'Sreekanthkodavati1')
      }
    }
    /*stage('Initialize') {
      steps {
        bat '''
                    export PATH=C:\Program Files\apache-maven-3.5.4
                    export M2_HOME=C:\Program Files\apache-maven-3.5.4
                '''
      }
    }*/
    stage('Build') {
      steps {
        echo 'build'
        /*sh 'mvn clean test'*/
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
}
