pipeline {
  agent any
  stages {
    stage('log tool') {
      parallel {
        stage('log tool') {
          steps {
            sh '''java -version
git --version
mvn --version'''
          }
        }

        stage('') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

  }
}