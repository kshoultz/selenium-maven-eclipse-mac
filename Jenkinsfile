pipeline {
  agent any
  tools {
  	maven 'MAVEN_HOME'
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