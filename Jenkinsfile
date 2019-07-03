node {
stage ('SCM checkout'){
git "https://github.com/hemrajchouhan/CucumberAzureJenkins.git"
}
stage ('Build'){
dir("cucumberjvm-selenium-keywordframework") {
sh "mvn clean install"
}
dir("cucumberjvm-selenium-keywordframework/target") {
sh "java -jar cucumberjvm-selenium-keywordframework-0.0.1.jar"
}
}
}
