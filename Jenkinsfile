pipeline {
    agent any
     // some
    stages {
        stage('Docker image Build') {
            steps {
                bat 'docker build -t myapp:${BUILD_NUMBER} .'
            }
        }
    }
}
