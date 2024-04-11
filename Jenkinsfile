pipeline {
    agent{
        label 'maven'
    }
    
    stages{
        stage('Git Checkout'){
            steps{
                git url: 'https://github.com/spring-projects/spring-petclinic.git',
                    branch: 'main'                    
            }
        }
        stage('Maven Compile'){
            steps{
                sh "/opt/apache-maven-3.9.6/bin/mvn compile"
            }
        }
    }
}