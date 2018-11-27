pipeline {
  agent any
  stages {
    stage('server') {
      agent {
        docker {
          image 'maven:3-alpine'
          args '-v /root/.m2:/root/.m2'
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