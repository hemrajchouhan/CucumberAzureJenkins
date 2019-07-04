
 node{
  stage ('Build') {
 
    git url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
 
    
  }
  stage('Smoke') {
     
     withMaven(...) {
 
      bat "mvn clean install"
 
         } 
      
        }
    
}

