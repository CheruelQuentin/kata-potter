pipeline {
  agent any
  stages {
    stage('Log Tool Version') {
      parallel {
        stage('Log Tool Version') {
          steps {
            sh '''mvn --version
git --version
java -version'''
          }
        }

        stage('Check for POM') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('Build with maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Post build Steps') {
      steps {
        writeFile(file: 'status.txt', text: 'Success')
      }
    }

  }
}