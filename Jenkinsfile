pipeline{
    
    tools{
        maven 'mymaven'
    }
    
    agent any
    
    stages{
        stage('Clone Repo'){
            steps{
                git 'https://github.com/PraveenPush/DevOpsCodeDemo.git'
        }
        
    }
    
        stage('Compile the Code'){
            steps{
                sh 'mvn compile'
            }
        }
        
        stage('Code Review'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        
        stage('Unit Test'){
            steps{
                sh 'mvn test'
            }
        }
        
        stage('Package'){
            steps{
                sh 'mvn clean install package'
            }
        }
        
    }
}
