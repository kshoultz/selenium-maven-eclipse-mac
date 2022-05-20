pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh '''java -version

git --version
mvn -v'''
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