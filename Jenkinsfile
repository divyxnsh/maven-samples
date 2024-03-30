pipeline {
  agent any
  stages {
    stage('check out ') {
      steps {
        git(url: 'https://github.com/divyxnsh/maven-samples.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
  environment {
    maven = '\'DHT_MVN\' '
    jdk = '\'DHT_SENSE\''
  }
}