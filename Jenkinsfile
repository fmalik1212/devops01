pipeline {
  agent any
  stages {
    stage('UNIT TESTING') {
      parallel {
        stage('TEST 1') {
          steps {
            sh '''java -version
'''
          }
        }

        stage('TEST 2') {
          steps {
            sh '''git --version
'''
          }
        }

        stage('TEST 3') {
          steps {
            sh 'mvn --version'
          }
        }

        stage('TEST 4') {
          steps {
            fileExists 'xyz.txt'
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