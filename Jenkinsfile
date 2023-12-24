pipeline {
  agent any
  stages {
    stage('Log Tool Versions') {
      parallel {
        stage('Log Tool Versions') {
          steps {
            sh 'java -version'
          }
        }

        stage('Check if Pom.xml Exists') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('Run tests') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Print success') {
      steps {
        echo 'Tests passed!'
      }
    }

  }
}