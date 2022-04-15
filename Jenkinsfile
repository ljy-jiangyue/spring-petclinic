pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''./mvnw package
cp -r ./target ~/target'''
      }
    }
    stage('jar') {
      steps {
       
          sh 'java -jar target/*.jar'
        
      }
    }
  }
}
