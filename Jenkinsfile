
pipeline {
  agent { 
    label 'slave_node_different_user'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package -Dmaven.buildDirectory=/targed'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Deliver') {
      steps {
        sh 'cp target/nomorepatience-1.0-SNAPSHOT.jar  ~'
      }
    }
  }
}  
