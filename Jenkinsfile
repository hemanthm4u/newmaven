pipeline {
    agent any
    tools {
        maven "maven3.6.6"
    }
    stages {
        stage('checkout&build') {
            steps {
                git 'https://github.com/hemanthm4u/newmaven'
                sh "mvn package"
            }
        }
          stage('deploy') {
            steps {
                sh "cp target/JenkinsWar.war /var/lib/tomcat9/webapps/"
            }
        }
    }
}
