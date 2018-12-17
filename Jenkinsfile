pipeline {
    agent none
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            agent {
                lable "some-label"
            }
            when {
                beforeAgent true
                branch 'master'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}