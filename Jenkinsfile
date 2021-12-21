pipeline {
    agent any
    stages {
        stage('Build') 
        {
          steps {
                sh "mvn clean install"
            }
        stage('copy') {
          steps {
                sh "cd /var/lib/jenkins/workspace/java/"
                sh "cp sparkjava-hello-world-1.0.war /var/lib/tomcat9/webapps/"
                sh "mvn clean install"
            }

    post {
        // If Maven was able to run the tests, even if some of the test
        // failed, record the test results and archive the jar file.
            success {
                echo "hello"
            }
            }
        }
    }
}
}
