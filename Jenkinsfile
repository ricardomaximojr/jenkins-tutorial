node {
    stage('Example') {
        try {
            sh 'exit 1'
        }
        catch (esc) {
            echo 'Something failed, I should sound the klaxons'
            // throw
        }
    }
}