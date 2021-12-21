pipeline {
    agent any
    stages {
        stage('Build') {
          steps {
                sh "mvn clean install"
            }
        }
        stage('copy') {
          steps {
                sh "cd /var/lib/jenkins/workspace/java/"
                sh "cp sparkjava-hello-world-1.0.war /var/lib/tomcat9/webapps/"
            }
        }
    }
}
