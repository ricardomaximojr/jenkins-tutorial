pipeline {
    agent any
    environment {
        DEPLOY_TO = 'master'
    }
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
                sh 'printenv'
            }
        }
        stage('Example Deploy') {
            when {
                branch 'production'
                anyOf {
                    environment name: 'DEPLOY_TO', value: 'production'
                    environment name: 'DEPLOY_TO', value: 'staging'
                }
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}