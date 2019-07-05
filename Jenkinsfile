node('master'){
   stage('Checkout'){
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git']]])
   }
  stage('Compile-Package'){      
   tool name: 'maven-3', type: 'maven'
   //dir('C:\\Program Files (x86)\\Jenkins\\workspace\\pipeline_selenium1\\cucumberjvm-selenium-keyword-framework') {
   //sh 'mvn package'
     bat label: '', script: 'mvn clean install'
  //}   
  }
  stage('SELENIUM TEST'){
     echo  'SANITY Testing'
  }
  stage('DEPLOY'){
     echo  'Unit Testing'
  } 
  stage('SANITY TESTING'){
     echo  'Unit Testing'
  } 
}
