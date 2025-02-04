pipeline {
    agent any

    stages {
        stage('git scm checkout') {
            steps {
                git 'https://github.com/kumargaurav039/maven-project.git'
            }
        }
        
        stage('compile') {
            steps {
                withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                sh 'mvn clean package' 
}
            }
        }
        stage('deploy on tomcat') {
            steps {
                sshagent(['DEVCICD']) {
                { sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@172.31.9.71:/usr/share/tomcat/webapps'  }
                    }
            }
        }
    }
}
