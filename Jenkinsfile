pipeline {
    agent any
    stages {
        stage('Non-Parallel Stage') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Parallel') {
            when {
                branch 'master'
            }
            failfast true
            parallel {
                stage('Branch A') {
                    agent {
                        docker {
                            image 'python:3.5.1'
                            // label 'for-branch-a'
                        }
                    }
                    steps {
                        echo 'On Branch A'
                    }
                }
                stage('Branch B') {
                    agent {
                        docker {
                            image 'maven:3.3.3'
                            // label 'for-branch-b'
                        }
                    }
                    steps {
                        echo 'On Branch B'
                    }
                }
                stage('Branch C') {
                    agent {
                        docker {
                            image 'node:6.3'
                            // label 'for-branch-c'
                        }
                    }
                    stages {
                        stage('Nested 1') {
                            steps {
                                echo 'In stage Nested 1 within Branch C'
                            }
                        }
                        stage('Nested 2') {
                            steps {
                                echo 'In stage Nested 2 within Branch C'
                            }
                        }
                    }
                }
            }
        }
    }
}