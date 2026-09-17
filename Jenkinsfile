pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['dev', 'staging', 'prod'],
            description: 'Select the deployment environment'
        )
    }

    stages {
        stage('Checkout') {
            steps {
                git(
                    branch: 'main',
                    url: 'https://github.com/spamyouracc-spec/para.git'
                )
            }
        }

        stage('Show Parameter') {
            steps {
                bat "echo Selected environment: ${params.ENVIRONMENT}"
            }
        }

        stage('Build for Environment') {
            steps {
                bat "echo Building the application for the ${params.ENVIRONMENT} environment..."
            }
        }
    }
}
