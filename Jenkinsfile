
 node{
  stage ('Build') {
 
    git url: 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
 
    
  }
  stage('Smoke') {
        try {
            sh "mvn clean install"
        } catch (err) {

        } finally {
            publishHTML (target: [
                    reportDir: 'target/*',
                    reportFiles: 'index.html',
                    reportName: "Smoke tests report"
            ])
        }
    }
}

