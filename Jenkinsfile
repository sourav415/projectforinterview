pipeline{
    
    agent any
    
    stages{
        
        stage('Build'){
            
            when{
                expression{
                    
                    env.BRANCH_NAME == 'dev'
                }
            }
            
            steps{
                
                echo "build my proj"
            }
        }
        
        stage('Test'){
            
            steps{
                
                echo "test my proj"
                
            }
        }
        
        stage('deploy'){
            
            steps{
                
                echo "deploy my proj"
            }
        }
    }
    
    post{
     
     always{
         
         echo "always exectue"
     }
        
    }
}
