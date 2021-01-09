pipeline {
    agent any
    parameters {
        choice(name: 'BROWSER', choices: ['chrome', 'firefox'], description: '')
        choice(name: 'SUREFIRE', choices: ['testng-smoke.xml', 'testng-all.xml'], description: '')
    }
    tools {
        maven '3.6.3'
      }
    stages {
        stage('Test') {
            steps {
               echo 'This is a minimal pipeline.'
                sh "mvn -Dbrowser=${BROWSER} -Dsurefire.suiteXmlFiles=${SUREFIRE} clean test"
            }
        }
    }
}
