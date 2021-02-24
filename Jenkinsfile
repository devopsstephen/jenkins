pipeline{
    
    agent any
    tools{
        
        maven 'mymaven'
        jdk 'myjava'
    }
    
    stages{
        stage ('checkout'){
            
            steps{
                
                git 'https://github.com/kliakos/sparkjava-war-example.git' 
            }
        }
      stage ('package'){
          steps{
              
              sh 'mvn clean package ' 
          }
      } 
      stage ('deploy'){
          steps{
              sh 'cp /root/.jenkins/workspace/dsljob/target/sparkjava-hello-world-1.0.war /opt'
          }
      }
    }
    post{
        
        always{
            
            sh 'rm -rf /root/.jenkins/workspace/dsljob/target/'
        }
    }
}
