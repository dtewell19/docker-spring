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
    stage('Deploy to Docker') {
      steps {
        sh 'docker run -p 8333:8333 -t springio/gs-spring-boot-docker'
      }
    }
  }
  environment {
    PATH = '/usr/local/opt/node@10/bin:/usr/local/opt/node@10/bin:/usr/local/sbin:/usr/local/Caskroom/google-cloud-sdk/latest/google-cloud-sdk/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Applications/Wireshark.app/Contents/MacOS'
  }
}