pipeline {
  agent any
  stages {
    stage('log tool version') {
      parallel {
        stage('log tool version') {
          steps {
            sh '''git --version
java -version'''
          }
        }

        stage('file exist') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
        tool(name: 'Maven 3.3.9', type: 'jdk8')
      }
    }

  }
}