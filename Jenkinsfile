pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/madeinnordeste/jenkins-blue-ocean-example.git', branch: 'master')
      }
    }
    stage('cat') {
      steps {
        sh 'cat index.php'
      }
    }
    stage('cp') {
      steps {
        sh 'cp index.php index2.php'
      }
    }
    stage('phpunit') {
      agent {
        dockerfile {
          filename 'Dockerfile'
        }
        
      }
      steps {
        sh 'phpunit --version'
      }
    }
  }
  environment {
    TESTEX = 'valor-do-testex'
  }
}