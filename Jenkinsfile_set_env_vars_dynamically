pipeline {
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    environment {
        // Using returnStdout
        CC = """${sh(
            returnStdout: true,
            script: 'echo "clang"'
        )}"""
        // Using returnStatus
        EXIT_STATUS = """${sh(
            returnStatus: true,
            script: 'exit 1'
        )}"""
    }
    stages {
        stage('Example') {
            environment {
                DEBUG_FLAGS = '-g'
            }
            steps {
                sh 'printenv'
            }
        }
    }
}