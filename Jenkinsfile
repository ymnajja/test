pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/ymnajja/test.git', branch: 'main')
      }
    }

    stage('log') {
      steps {
        sh 'ls -al'
      }
    }

  }
}