pipeline {
    agent any
    
    environment {
        DOCKER_IMAGE = "sumanthvarma002/my-python-app"
    }

    stages {
        
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/SumanthvarmaJS/Devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Push Image to DockerHub') {
            steps {
                sh 'docker push $DOCKER_IMAGE'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm $DOCKER_IMAGE'
            }
        }

    }
}
