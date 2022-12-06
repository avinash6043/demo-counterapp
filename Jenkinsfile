pipeline{
    
    agent any 
    environment{
        PATH= "/usr/share/maven/bin:$PATH"
    }
    stages {
        
        stage('Git Checkout'){
            
            steps{
                git credentialsId: 'github', url: 'https://github.com/avinash6043/demo-counterapp.git'
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
