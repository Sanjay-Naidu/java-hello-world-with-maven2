pipeline {
    agent any


    stages {
        stage('Checkout') {
            steps {
                git branch: "${master}", url: "${https://github.com/Sanjay-Naidu/java-hello-world-with-maven2}"
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded!'
        }
        failure {
            echo '❌ Build failed.'
        }
    }
}
