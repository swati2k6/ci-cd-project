pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("ci-cd-app")
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    docker.run("-d -p 5000:5000 ci-cd-app")
                }
            }
        }
    }
}