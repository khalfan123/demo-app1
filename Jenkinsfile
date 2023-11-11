pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using Dockerfile
                    def dockerImage = docker.build('demo-app1', '-f ./Dockerfile .')

                    // Tag the built image
                    dockerImage.tag('777229646641.dkr.ecr.us-east-1.amazonaws.com/demo-app1:latest')
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
