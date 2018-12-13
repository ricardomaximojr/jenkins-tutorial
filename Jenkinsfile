pipeline {
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    environment {
        AWS_ACCESS_KEY_ID = credentials('ricmaxjr')
        AWS_SECRET_ACCESS_KEY = credentials('ricmaxjr')
    }
    stages {
        stage('Build') {
            steps {
                sh "aws s3 ls"
            }
        }
    }
}