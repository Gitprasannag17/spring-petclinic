node('build-jdk17-mvn3.9.4_1') {
    stage('Git Checkout') {
        git branch: 'main', url: 'https://github.com/Gitprasannag17/spring-petclinic.git'
    }
    stage('build') {
        sh '/usr/local/apache-maven-3.9.4/bin/mvn clean package'
    }
    stage('archive') {
    archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
    }
}