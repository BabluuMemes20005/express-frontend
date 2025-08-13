pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/BabluuMemes20005/express-frontend.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t express-frontend .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3000:3000 express-frontend'
            }
        }
    }
}
