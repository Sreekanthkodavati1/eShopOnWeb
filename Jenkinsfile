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
        bat 'dotnet build eShopOnWeb.sln'
      }
    }
    stage('test') {
      steps {
        bat 'dotnet test eShopOnWeb.sln'
      }
    }
  }
}
