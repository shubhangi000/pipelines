pipeline {
    agent any

    stages {
        stage('git scm checkout') {
            steps {
                git 'https://github.com/shubhangi000/maven-project.git'
            }
        }
        
        stage('compile') {
            steps {
                withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn validate' 
                }
            }
        }
        
        

        
    }
}
