pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh 'echo building the application...'
          }
        }

        stage('Adding a log') {
          steps {
            git(url: 'https://github.com/fnahum/jenkins-demo', branch: 'dev')
          }
        }

      }
    }

    stage('test') {
      steps {
        sh 'echo \'testing the application...\''
      }
    }

    stage('deploying') {
      steps {
        sh 'echo \'deploying the application...\''
      }
    }

  }
}