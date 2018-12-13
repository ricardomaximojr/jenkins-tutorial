pipeline {
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    stages {
        stage('build') {
            steps {
                def singlyQuoted = 'Hello'
                def doublyQuoted = "World"
                
                def username = 'Jenkins'
                echo 'Hello Mr. ${username}'
                echo "I said, Hello Mr. ${username}"
            }
        }
    }
}