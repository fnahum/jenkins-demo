pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo Construyendo el codigo ...'
          }
        }

        stage('Indexing') {
          steps {
            git(url: 'https://github.com/fnahum/jenkins-demo', branch: 'dev')
          }
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo Probando el codigo'
      }
    }

    stage('Deploy') {
      steps {
        sh 'echo Entregando el codigo'
      }
    }

  }
}