pipeline {
  agent {
    docker {
      image 'maven:3.6.3-jdk-8'
    }

  }
  stages {
    stage('PREP') {
      steps {
        sh 'echo hello world'
        echo 'message'
      }
    }

    stage('compile') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        sh 'mvn package'
      }
    }

    stage('archile') {
      steps {
        junit '*.xml'
      }
    }

  }
  environment {
    USER_NAME = 'RAHUL'
  }
}
