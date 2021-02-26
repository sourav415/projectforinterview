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
                
                withCredentials([usernamePassword(credentialsId: 'github', passwordVariable: 'pwd', usernameVariable: 'uname')]) {
                    bat "build my proj ${uname}"
                    }
                
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
