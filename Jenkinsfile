node {
    stage ('Build') {
        git branch:'master', url: 'git@bitbucket.org:anahata/anahata-pom.git'
        withMaven (
            maven: 'Maven 3.8.6',
            jdk: 'JDK 1.8') {
                sh "mvn -Dmaven.test.skip=true clean install deploy"
            } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
    }
    
    
}