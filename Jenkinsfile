pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'inicializando'
      }
    }

    stage('bulid maven') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
      }
    }

  }
}