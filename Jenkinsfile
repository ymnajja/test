pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/ymnajja/test.git', branch: 'main')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -al'
          }
        }

        stage('front-end unit') {
          steps {
            sh 'cd curriculum-front '
            sh 'npm install --save-dev vue-jest'
            sh 'npm -i'
            sh 'npm test:unit'
          }
        }

      }
    }

  }
}