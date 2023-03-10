pipeline {
    agent { label 'jdk_8' }
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/TEJA79955/spring-petclinic.git'
                    branch: 'main'
            }
        }
        stage('package') {
            steps {
                sh 'export PATH=/usr/lib/jvm/java-17-openjdk-amd64/bin:$PATH'
                sh 'mvn package'
            }
        }
    }
}            