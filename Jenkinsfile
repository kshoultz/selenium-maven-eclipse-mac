pipeline {
  agent any
  tools {
  	maven 3.8.5
  }
  stages {
    stage('Log Tool Versions') {
      steps {
        sh '''
        	java -version
			git --version
			mvn -v
		'''
      }
    }

    stage('Build Maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Test Maven') {
      steps {
        sh 'echo test'
      }
    }

  }
}