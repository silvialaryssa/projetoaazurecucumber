pipeline {
  agent any
  tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
  stages {
    stage('build') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
      }
    }

    stage('bulid maven') {
      steps {
       sh 'mvn -Dmaven.test.failure.ignore=true install' 
      }
      post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
    }

  }
}
