node('master'){
   def mvn = tool (name: 'maven3', type: 'maven') + '/bin/mvn'
   
   stage('Checkout'){
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git']]])
   }
  stage('Compile-Package'){      
   //tool name: 'maven-3', type: 'maven'
   dir('C:\\Program Files (x86)\\Jenkins\\workspace\\pipeline_selenium1\\cucumberjvm-selenium-keyword-framework') {
     tool name: 'JAVA_HOME', type: 'jdk'
     bat label: '', script: 'mvn clean install'
  }   
  }
  stage('SELENIUM CUCUMBER TEST REPORT'){
    cucumber failedFeaturesNumber: -1, failedScenariosNumber: -1, failedStepsNumber: -1, fileIncludePattern: '**/*.json', pendingStepsNumber: -1, skippedStepsNumber: -1, sortingMethod: 'ALPHABETICAL', undefinedStepsNumber: -1
  }
  stage('DEPLOY'){
     echo  'Unit Testing'
  } 
  stage('SANITY TESTING'){
     echo  'Unit Testing'
  } 
    stage('Email Notification'){
		mail bcc: '', body: """Hi Team, You build successfully deployed
		                       Job URL : ${env.JOB_URL}
							   Job Name: ${env.JOB_NAME}
   Thanks,
   DevOps Team""", cc: '', from: '', replyTo: '', subject: "${env.JOB_NAME} Success", to: 'hemrajchouhan1989@gmail.com'
   
   }
}
