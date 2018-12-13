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
        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
    }
}