pipeline {
    agent any

    environment {
        DOCKER_IMAGE_NAME = 'docker.io/engsabry/nginx-argo'
        DOCKER_IMAGE_TAG = 'latest'
    }


    stages {
        stage('Code Checkout') {
            steps {
                echo 'Code Checkout'
                checkout scm
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    echo "Building docker image $DOCKER_IMAGE_NAME:$DOCKER_IMAGE_TAG"
                    docker.Build("$DOCKER_IMAGE_NAME:$DOCKER_IMAGE_TAG")
                    
                }
            }
        }
        stage('Push Docker Image') {
            steps {
                script {
                    echo
                    docker.Push("$DOCKER_IMAGE_NAME:$DOCKER_IMAGE_TAG")
                    
                }
            }
        }
    }
}