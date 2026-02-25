pipeline {
    agent any
    
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/SumanthvarmaJS/Devops.git'
            }
        }
        
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-python-app .'
            }
        }
        
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 my-python-app'
            }
        }
    }
}
