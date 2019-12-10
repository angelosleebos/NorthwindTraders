pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/angelosleebos/NorthwindTraders', branch: 'master')
        openshiftDeploy 'dotnetcore22'
      }
    }
    stage('Deploy') {
      steps {
        openshiftDeploy 'dotnetcore22'
      }
    }
  }
}