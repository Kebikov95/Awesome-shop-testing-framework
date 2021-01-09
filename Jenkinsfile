pipeline {
    agent any
    tools {
        maven '3.6.3'
      }
    stages {
        stage('Test') {
            steps {
               echo 'This is a minimal pipeline.'
               sh "mvn clean test"
            }
        }
    }
}
