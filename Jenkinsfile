pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh '''java -version
mvn -v
git --version
'''
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