pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using Dockerfile
                    docker.build('777229646641.dkr.ecr.us-east-1.amazonaws.com/demo-app1:${BUILD_TAG}', '-f ./Dockerfile .')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // Run Docker container from the built image on port 80
                    sh 'docker run -d -p 80:80 777229646641.dkr.ecr.us-east-1.amazonaws.com/demo-app1:${BUILD_TAG}'
                }
            }
        }
    }
}
