pipeline {
    agent any
    environment {
		DOCKERHUB_CREDENTIALS=credentials('vskartdocker-dockerhub')
	}

    stages {
        stage('Build and Deploy') {
            steps {

                
                bat 'sudo docker build -t vskartdocker/dockerrepo1:1.0 .'
                bat 'sudo chmod 666 /var/run/docker.sock'
                bat 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
                bat 'docker push vskartdocker/dockerrepo1:1.0'
        }      
        }
        
    }
}
