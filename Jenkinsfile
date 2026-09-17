pipeline{
agentany
parameters{
choice(name: 'ENVIRONMENT', choices:['dev','staging', 'prod'],description: 'Selectthedeploymentenvironment'
}
stages{
stage('Checkout') {
steps{
gitbranch: 'main', url: 'https://github.com/spamyouracc-spec/para.git'
}
}
stage('ShowParameter'){
steps{
bat "Selectedenvironment: ${params.ENVIRONMENT}"
}
}
stage('BuildforEnvironment') {
steps{
bat "Buildingthe applicationforthe ${params.ENVIRONMENT} environment..."
}
}
}
}
