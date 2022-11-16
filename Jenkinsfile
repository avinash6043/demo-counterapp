pipeline{
    
    agent any 
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                git branch: 'main', url: 'https://github.com/nani059/demo-counterapp.git'
            }
        }    
        stage('UNIT testing'){

            steps{
                sh 'mvn test'
            }
        }
        stage('Maven build'){

            steps{
                sh 'mvn clean install'
            }
        }
        stage('SonarQube analysis'){
           steps{
               script{
                    withSonarQubeEnv(credentialsId: 'sonarapi-key'){
                     sh 'mvn clean package sonar:sonar'
               }
           }
        }
    }
}

