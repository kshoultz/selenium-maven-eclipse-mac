pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('Log Tool Versions') {
          steps {
            sh '''java -version
git --version'''
          }
        }

        stage('compile maven') {
          steps {
            sh 'mvn compile test package'
          }
        }

      }
    }

  }
}