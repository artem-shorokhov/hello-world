node {
    try {
        stage('Checkout') {
            checkout scm
        }

        stage('Build') {
            sh './gradlew build'
        }
        
        if ($BRANCH_NAME.startsWith('release')) {
            stage('release') {
                sh 'echo Attention! Releasing!'
            }
        }
    } catch(e) {
        throw e
    }
}
