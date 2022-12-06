pipeline{
    
    agent any 
 
    stages {
        
        stage('Git Checkout'){
            
            steps{
                git credentialsId: 'github', url: 'https://github.com/avinash6043/demo-counterapp.git'
            }
        }    
        
        
    }
}
}
