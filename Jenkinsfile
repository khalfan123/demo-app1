pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image
                    docker.build('your-image-name')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // Run Docker container
                    docker.image('your-image-name').run('-d -p 8080:8080')
                }
            }
        }
    }
}
