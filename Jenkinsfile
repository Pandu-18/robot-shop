pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Pandu-18/robot-shop.git'
            }
        }

        stage('Verify Root Structure') {
            steps {
                sh 'ls -l'
            }
        }

        stage('CI Checks') {
            steps {
                echo 'Robot-Shop CI pipeline executed successfully!'
            }
        }
    }
}
