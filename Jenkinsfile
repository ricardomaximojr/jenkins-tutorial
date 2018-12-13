pipeline {
    environment {
        username = "Jenkins"
    }
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    stages {
        stage('build') {
            steps {
                sh '''
                    echo 'Hello Mr. ${username}'
                    echo "I said, Hello Mr. ${username}"
                '''
            }
        }
    }
}