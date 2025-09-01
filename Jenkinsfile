pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Pandu-18/robot-shop.git'
            }
        }

        stage('Build Frontend Image') {
            steps {
                sh '''
                cd roboshop/docker/frontend
                docker build -t robot-shop-frontend .
                '''
            }
        }
    }
}
