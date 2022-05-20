pipeline {
  agent any
  stages {
    stage('Log Tool Versions') {
      steps {
        tool(name: 'maven', type: 'MAVEN_HOME')
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