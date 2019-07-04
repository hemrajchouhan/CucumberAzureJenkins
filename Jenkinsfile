node{
stage('Git checkout') { // for display purposes
        git 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
    }
    stage('Smoke') {
        try {
            sh "mvn clean install"
        } catch (err) {

        } finally {
            publishHTML (target: [
                    reportDir: 'target/*',
            ])
        }
    }
}
