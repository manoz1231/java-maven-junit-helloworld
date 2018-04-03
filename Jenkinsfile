pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('performance test') {
      steps {
        sh 'mvn verify'
      }
    }
    stage('finish') {
      steps {
        sh 'echo "build has been done !"'
      }
    }
  }
}