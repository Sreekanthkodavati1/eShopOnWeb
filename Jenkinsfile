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
    stage('test') {
      steps {
        sh 'dotnet test eShopOnWeb.sln'
      }
    }
  }
}
