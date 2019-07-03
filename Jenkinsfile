node {
 
   stage('Git checkout') { // for display purposes
      git 'https://github.com/hemrajchouhan/CucumberAzureJenkins.git'
   }
    

    stage ('Compile Stage') {

            steps {

                withMaven(maven: 'maven_3_5_0') {
                    sh 'mvn clean install'

                }

            }
    }
}
