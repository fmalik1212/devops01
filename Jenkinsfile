pipeline {
  agent any
  stages {
    stage('log tool') {
      steps {
        sh '''java -version
git --version
mvn --version'''
      }
    }

  }
}