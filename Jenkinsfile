pipeline {
  agent any
  stages {
    stage('Log tool version') {
      parallel {
        stage('Log tool version') {
          steps {
            sh '''mvn --version
git --version
java --version'''
          }
        }

        stage('check for POM') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('build with Maven') {
      steps {
        sh 'mvn complie test package'
      }
    }

  }
}