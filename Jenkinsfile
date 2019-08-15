pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '/usr/local/bin/mvn package'
      }
    }
    stage('Containerize ') {
      steps {
        sh '/usr/local/bin/mvn install dockerfile:build'
      }
    }
  }
}