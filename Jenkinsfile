pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                withMaven (maven: 'Maven 3.9.8', jdk: 'JDK 1.8') {
                    sh "mvn -Dmaven.test.skip=true clean install deploy"
                } 
            }
        }
    }
}