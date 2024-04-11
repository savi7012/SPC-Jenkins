pipeline {
    agent{
        label 'maven'
    }
    environment {
        mvn = '/opt/apache-maven-3.9.6/bin/mvn'
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
                sh "$mvn compile"
            }
        }
    }
}