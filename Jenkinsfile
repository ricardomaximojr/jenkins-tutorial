pipeline {
    agent none
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            when {
                beforeInput true
                branch 'master'
            }
            input {
                message 'Deploy to production?'
                id 'simple-input'
            }
            steps {
                echo 'Deployting'
            }
        }
    }
}