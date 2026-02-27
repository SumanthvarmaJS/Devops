pipeline {
    agent any
    
    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/SumanthvarmaJS/Devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sumanthvarma002/my-python-app .'
            }
        }

        stage('Docker Login') {
            steps {
                sh 'docker login -u sumanthvarma002 -p Sumanth123'
            }
        }

        stage('Push Image to DockerHub') {
            steps {
                sh 'docker push sumanthvarma002/my-python-app'
            }
        }

    }
}
