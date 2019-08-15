pipeline {
  agent any
  environment {
    PATH = "/usr/local/opt/node@10/bin:/usr/local/opt/node@10/bin:/usr/local/sbin:/usr/local/Caskroom/google-cloud-sdk/latest/google-cloud-sdk/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Applications/Wireshark.app/Contents/MacOS"
  }
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
