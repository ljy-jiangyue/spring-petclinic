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
       
          sh 'ansible-playbook playbook.yaml --private-key /.ssh/id_rsa -i hosts'
        
      }
    }
  }
}
