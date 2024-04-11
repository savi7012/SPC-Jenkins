pipeline {
    agent{
        label 'maven'
    }
    triggers{
        cron('* * * * *')
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
                
            }
        }

    }
}