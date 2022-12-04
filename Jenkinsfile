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

        stage('error') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('Build the code') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Post build job') {
      steps {
        writeFile(file: 'Status.txt', text: 'it worked! ')
      }
    }

  }
}