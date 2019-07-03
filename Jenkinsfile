node {
   stage('Git checkout') { // for display purposes
      git 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
   }
   stage('Smoke') {
            sh "mvn clean install'"
   }
   stage('Results') {
     '**/target/*.html'
   }
}
