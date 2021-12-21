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
                sh "cd /var/lib/jenkins/workspace/Java_Job/target/"
                sh "cp sparkjava-hello-world-1.0.war /var/lib/tomcat9/webapps/"
            }
        }
    }
    post {
        always {
            cleanWs()
        } 
}
