node {
   stage('Git checkout') { // for display purposes
      git 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
   }
   stage('Smoke') {
        try {
            sh "mvn clean install'"
        } catch (err) {
            
        } finally {
            publishHTML (target: [
            reportDir: 'target',
            reportFiles: 'index.html',
            reportName: "Selenium tests report"
            ])
        }
   }
   stage('Results') {
      junit '**/target/cucumber-html-report/*.html'
   }
}
