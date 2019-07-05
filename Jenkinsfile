node('master'){
 
   stage('Checkout'){
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git']]])

   }
  // stage('Compile-Package'){      
  //     def MVNHOME=tool name: 'MAVEN_HOME', type: 'maven'
  //   sh "${MVNHOME}/bin/mvn package"
  // }
   
 stage ('Build'){
   def MVNHOME=tool name: 'MAVEN_HOME', type: 'maven'
        sh "${MVNHOME}/bin/mvn clean install"
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
