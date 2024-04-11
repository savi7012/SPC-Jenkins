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
        stage('Maven Test'){
            steps{
                sh "$mvn test"
            }
        }
        stage('Maven Package'){
            steps{
                sh "$mvn clean package"
            }
        }
    }
}