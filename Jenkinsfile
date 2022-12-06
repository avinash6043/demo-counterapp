pipeline{
    
    agent any 
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                git credentialsId: 'github', url: 'https://github.com/avinash6043/demo-counterapp.git'
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
        
    }
}
}
