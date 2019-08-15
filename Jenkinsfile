pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }
    stage('Containerize ') {
      steps {
        sh 'mvn install dockerfile:build'
      }
    }
  }
}