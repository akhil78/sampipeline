pipeline {
  agent any
  stages {
    stage('server') {
      agent {
        docker {
          image 'maven:3.5-jdk-8-slim'
        }

      }
      steps {
        sh '''echo " server"
mvn -version
mkdir -p target
touch "target/server.war"'''
      }
    }
  }
}