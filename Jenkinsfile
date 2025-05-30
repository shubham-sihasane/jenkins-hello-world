pipeline {
  agent any
  tools {
    maven 'M3'
  }
  stages {
    stage('Git Checkout') {
       steps {
         git branch: 'main', url: 'https://github.com/shubham-sihasane/jenkins-hello-world.git'
       }
     } 
    stage('Build) {
      steps {
        sh 'mvn clean package -DskipTests=true'
      }
    }
    stage('Test) {
      steps {
        sh 'mvn test'      
      }
    }
  }
}
