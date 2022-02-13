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
      parallel {
        stage('Build with maven') {
          steps {
            sh 'mvn compile test package'
          }
        }

        stage('Unit Test') {
          steps {
            sh 'mvn test'
          }
        }

        stage('Checkstyle') {
          steps {
            sh 'mvn checkstyle:checkstyle'
          }
        }

        stage('PMD') {
          steps {
            sh 'mvn pmd:pmd'
          }
        }

      }
    }

    stage('Post build Steps') {
      steps {
        writeFile(file: 'status.txt', text: 'Success')
      }
    }

  }
}