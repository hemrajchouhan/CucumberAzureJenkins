node {
stage ('SCM checkout'){
git "https://github.com/hemrajchouhan/CucumberAzureJenkins.git"
}
stage ('Build'){
dir("cucumberjvm-selenium-keywordframework") {
sh "mvn clean install"
}
}
}
