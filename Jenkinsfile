pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Pandu-18/robot-shop.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t robot-shop .'
            }
        }

        stage('Run Application') {
            steps {
                sh 'docker run -d -p 8081:8080 --name robot-shop robot-shop'
            }
        }
    }
}
