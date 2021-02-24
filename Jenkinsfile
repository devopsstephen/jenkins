pipeline {
   agent any
stages{
      stage ('checkout'){
      steps{
         echo 'hello'
}

}

stage ('package'){
    
    steps{
        
        echo 'creatingmvn package'
    }
}


stage ('deploy'){
    
    steps{
        echo 'deploy'
    }
    
}
}
post {
   always{
       
       echo 'delete workspace'
   } 
    
}
}
 
 
