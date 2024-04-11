pipeline {
    agent{
        label 'maven-master'
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
                sh "mvn compile"
            }
        }
    }
}