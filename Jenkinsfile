pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/madeinnordeste/jenkins-blue-ocean-example.git', branch: 'master', changelog: true)
      }
    }
    stage('cat') {
      steps {
        sh 'cat index.php'
      }
    }
  }
}