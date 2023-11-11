pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using Dockerfile
                    sh 'docker build -t demo-app1 .'
                }
            }
        }

        // stage('Run Docker Container') {
        //     steps {
        //         script {
        //             // Run Docker container from the built image on port 80
        //             docker.image('demo-app1:latest').withRun('-p 80:80') {
        //                 // Perform any additional steps inside the running container if needed
        //             }
        //         }
        //     }
        // }
    }
}
