pipeline {
    agent any
    parameters {
        choice(name: 'browser', choices: ['chrome', 'firefox'], description: '')
        choice(name: 'surefire', choices: ['testng-smoke.xml', 'testng-all.xml'], description: '')
    }
    tools {
        maven '3.6.3'
      }
    stages {
        stage('Test') {
            steps {
               echo 'This is a minimal pipeline.'
                sh "mvn -Dbrowser=${browser} -Dsurefire.suiteXmlFiles=${surefire} clean test"
            }
        }
    }
}
