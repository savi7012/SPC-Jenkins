pipeline {
    agent { label 'maven-master' }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
            }
        }
        stage('MVN Validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('MVN Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('MVN Package') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
