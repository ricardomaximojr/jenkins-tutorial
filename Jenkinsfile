pipeline {
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh """
                    echo "Test failed"
                    exit 1
                """
            }
        }
    }
    post {
        always {
            echo 'This will be printed always!'
        }
        failure {
            mail to: "ricardomaximojr@gmail.com", 
                 subject: 'The Pipeline failed :(',
                 body: "Pipeline failed due to exit 1 sh step"
        }
    }
}