pipeline {
    agent any
    parameters {
	    string(name:'FROM_BUILD', defaultValue: '', description: 'build source')
    }
    stages {
        stage('Build') {
          steps {
                sh "mvn clean install"
            }
        }
        stage('copy') {
           steps {
		sh "rm -Rf /var/lib/tomcat9/webapps/sparkjava-hello-world-1.0.war"
                sh "cp /var/lib/jenkins/workspace/Java_Job/target/sparkjava-hello-world-1.0.war /var/lib/tomcat9/webapps/"
            }
        }
    }
	post {
		always {
			echo "Successful"
			cleanWs()
		}
	}
}
