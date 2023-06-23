pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/TaraGithub/curriculum-app.git', branch: 'dev')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front-end unit test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}