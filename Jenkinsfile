pipeline{
agentany
parameters{
choice(name: 'ENVIRONMENT', choices:['dev','staging', 'prod'],description: 'Selectthedeploymentenvironment'
}
stages{
stage('Checkout') {
steps{
gitbranch: 'main', url: 'https://github.com/<student-username>/<repo-name>.git'
}
}
stage('ShowParameter'){
steps{
echo "Selectedenvironment: ${params.ENVIRONMENT}"
}
}
stage('BuildforEnvironment') {
steps{
echo "Buildingthe applicationforthe ${params.ENVIRONMENT} environment..."
}
}
}
}
