node('master'){
   stage('Checkout'){
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git']]])
   }
  stage('Compile-Package'){      
   tool name: 'MAVEN_HOME', type: 'maven'
   dir('C:\\Program Files (x86)\\Jenkins\\workspace\\pipeline_selenium1\\cucumberjvm-selenium-keyword-framework') {
    sh 'mvn package'
  }   
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
