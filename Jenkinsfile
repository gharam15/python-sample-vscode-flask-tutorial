@Library('libx') _

pipeline {
     agent { 
        label 'java' 
    }
    environment {
        IMAGE_NAME = 'gharam/python-task'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                buildDockerImage(env.IMAGE_NAME)
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub-cred', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
                    pushDockerImage(env.IMAGE_NAME)
                }
            }
        }
    }
}