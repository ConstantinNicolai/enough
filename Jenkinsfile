
pipeline {
  agent { 
    label 'slave_node_different_user'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}  
