pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using Dockerfile
                    docker.build('777229646641.dkr.ecr.us-east-1.amazonaws.com/demo-app1', '-f ./Dockerfile .')
                }
            }
        }

        stage('Stop Existing Container') {
            steps {
                script {
                    // Check if the container exists by name and stop it
                    sh "docker ps -q --filter 'name=demo-app1-container' | xargs docker stop || true"
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // Run Docker container from the built image on port 80
                    sh 'docker run -d -p 80:80 --name=demo-app1-container 777229646641.dkr.ecr.us-east-1.amazonaws.com/demo-app1:latest'
                }
            }
        }
    }
}
