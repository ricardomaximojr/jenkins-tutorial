pipeline {
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh """
                    aws s3 ls
                """
            }
        }
    }
}