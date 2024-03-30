pipeline {
  agent any
  stages {
    stage('check out ') {
      steps {
        git(url: 'https://github.com/divyxnsh/maven-samples.git', branch: 'master')
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}