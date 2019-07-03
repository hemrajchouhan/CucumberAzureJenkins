
 node{
  stage ('Build') {
 
    git url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
 
    
  }
  stage('Smoke') {
     
            sh "mvn clean install"
      
        }
    
}

