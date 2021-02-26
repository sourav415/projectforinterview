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
                
                echo "Hi"
                
            }
        }
        
        stage('Test'){
            
            steps{
                
                   withCredentials([usernamePassword(credentialsId: 'github', passwordVariable: 'pwd', usernameVariable: 'uname')]) {
                    bat "build my proj ${uname}"
                    }
                
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
