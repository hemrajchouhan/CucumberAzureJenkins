node {
stage (‘SCM checkout’){
git “https://github.com/hemrajchouhan/CucumberAzureJenkins.git”
}
stage (‘Build’){
dir(“comtest”) {
sh “mvn clean install”
}
dir(“comtest/target”) {
sh “java -jar cucumberjvm-selenium-keywordframework-0.0.1.jar”
}
}
}
