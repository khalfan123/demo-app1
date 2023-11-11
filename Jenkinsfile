pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    def imageName = "demo-app1:${env.BUILD_NUMBER}
                    // Build Docker image using Dockerfile
                    docker.build('777229646641.dkr.ecr.us-east-1.amazonaws.com/${imageName}', '-f ./Dockerfile .')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    def imageName = "demo-app1:${env.BUILD_NUMBER}
                    // Run Docker container from the built image on port 80
                    sh 'docker run -d -p 80:80 777229646641.dkr.ecr.us-east-1.amazonaws.com/${imageName}'
                }
            }
        }
    }
}
