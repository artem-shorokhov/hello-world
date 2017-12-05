node {
    try {
        stage('Checkout') {
            checkout scm
        }

        stage('Build') {
            sh './gradlew build'
        }
    } catch(e) {
        throw e
    }
}
