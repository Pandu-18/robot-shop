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
                dir('robot-shop/docker/frontend') {
                    sh 'docker build -t robot-shop-frontend .'
                }
            }
        }

        stage('Run Application') {
            steps {
                sh 'docker run -d -p 8081:8080 --name robot-shop-frontend robot-shop-frontend'
            }
        }
    }
}
