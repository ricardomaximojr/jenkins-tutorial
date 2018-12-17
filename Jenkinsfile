pipeline {
    agent any
    stages {
        stage('Example') {
            input {
                message 'Should we continue?'
                ok 'Yes, we should.'
                submitter 'rmaximo'
                parameters {
                    string(
                        name: 'PERSON',
                        defaultValue: 'Mr Jenkins',
                        description: 'Who should I say hello to?'
                    )
                }
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you"
            }
        }
    }
}