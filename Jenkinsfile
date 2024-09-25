pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/manahilshakeel20I-2302/MLOPs_Class_Task-3.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('ImageJenkins')
                }
            }
        }

        stage('Push Docker Image to Docker Hub') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', 'c5027272-a513-4734-aa5d-c3376a5e8bd5') {
                        docker.image('ImageJenkins').push('latest')
                    }
                }
            }
        }

        stage('Pull Docker Image') {
            steps {
                script {
                    docker.image('ImageJenkins:latest').pull()
                }
            }
        }
    }
}