pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
                sh 'printenv'
            }
        }
        stage('Example Deploy') {
            when {
                allOf {
                    branch 'master'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}