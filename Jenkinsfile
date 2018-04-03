pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('testing') {
      steps {
        sh 'mvn test'
      }
    }
    stage('performance-test') {
      steps {
        sh 'mvn verify'
      }
    }
    stage('result') {
      steps {
        sh 'echo \'Am done with the build\''
      }
    }
  }
}