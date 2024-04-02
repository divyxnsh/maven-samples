pipeline {
  agent any
  stages {
    stage('fetch') {
      steps {
        sh 'git fetch origin 198644632661c67b6c32f59e9047c11a70685e15:new'
      }
    }

    stage('checkout') {
      steps {
        sh 'git checkout 198644632661c67b6c32f59e9047c11a70685e15'
      }
    }

    stage('bisect start') {
      steps {
        sh 'git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
      }
    }

    stage('run') {
      steps {
        sh 'git bisect run mvn clean test'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
  environment {
    maven = '\'DHT_MVN\''
    jdk = '\'DHT_SENSE\''
  }
}