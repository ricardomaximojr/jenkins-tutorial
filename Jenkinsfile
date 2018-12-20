pipeline {
    agent none
    stages {
        stage('Non-Sequential Stage') {
        agent {
            docker {
                image 'maven:3-alpine'
                args '-v /tmp:/tmp'
            }
        }
            steps {
                echo "On Non-Sequential Stage"
            }
        }
        stage('Sequential') {
            agent {
                docker {
                    image 'python:3.5.1'
                }
            }
            environment {
                FOR_SEQUENTIAL = 'some-value'
            }
            stages {
                stage('In Sequential 1') {
                    steps {
                        echo 'In Sequential 1'
                    }
                }
                stage('In Sequential 2') {
                    steps {
                        echo 'In Sequential 2'
                    }
                }
                stage('Parallel in Sequential') {
                    parallel {
                        stage('In Parallel 1') {
                            steps {
                                echo 'In Parallel 1'
                            }
                        }
                        stage('In Parallel 2') {
                            steps {
                                echo 'In Prallel 2'
                            }
                        }
                    }
                }
            }
        }
    }
}