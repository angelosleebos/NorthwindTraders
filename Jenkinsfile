pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/angelosleebos/NorthwindTraders', branch: 'dotnetcore22')
        openshiftDeploy 'webapp02'
      }
    }
    stage('Deploy') {
      steps {
        openshiftDeploy 'webapp02'
      }
    }
  }
}