pipeline {
  agent any
  stages {
    stage('Git checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/available-nick44/Hello.git'
      }
    }

    stage('Compile') {
      steps {
        sh 'javac Hello.java'
      }
    }

    stage('Run') {
      steps {
        sh 'java Hello'
      }
    }
  }

  post {
  	always {
  		echo "this is always"
  	}
  	success {
  		echo "this is success"
  	}
  	failure {
  		echo "this is failure"
  	}
  	unstable {
  		echo "this is unstalbe"
  	}
  	changed {
  		echo "this is changed"
  	}
  }
}
