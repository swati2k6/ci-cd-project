pipeline {
    agent any

    stages {
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
                    docker.run("-d -p 5001:5000 ci-cd-app")
                }
            }
        }
    }
}
