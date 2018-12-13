pipeline {
    agent {
        docker {
            image 'python:3.5.1'
        }
    }
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting} World"
            }
        }
    }
}