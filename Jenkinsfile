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
                    ls -l
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
            mail to: 'ricardomaximojr@gmail.com', 
                 subject: "Failed Pipeline: ${currentBuild.fullDisplayName}
                 body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}