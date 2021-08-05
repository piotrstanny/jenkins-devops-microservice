// SCRIPTED COMMANDS
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
//   stage('Integration Test') {
// 		echo "Integration Test"
// 	}
// }

// DECLARATIVE COMMANDS
pipeline {

  agent any

  environment {
    dockerHome = tool 'myDocker'
    mavenHome = tool 'myMaven'
    PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
  }

  stages {
    stage ('Build') {
      steps {
        sh 'mvn --version'
        sh 'docker version'
        echo "Build"
        echo "PATH - $PATH"
      }
    }
    stage ('Test') {
      steps {
        echo "Test"
      }
    }
    stage ('Integration Test') {
      steps {
        echo "Integration Test"
      }
    }
  }
}

