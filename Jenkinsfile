pipeline {
    agent any
    stages {
        stage('Docker image Build') {
            steps {
                sh 'docker build -t myapp:${BUILD_NUMBER} .'
            }
        }
    }
}