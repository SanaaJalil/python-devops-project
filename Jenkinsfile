pipeline {
    agent any

    stages {
        stage('Check Docker Version') {
            steps {
                script {
                    echo 'Checking if Docker is available...'
                }
                sh 'docker --version'
            }
        }

        stage('Pull Python Docker Image') {
            steps {
                echo 'Pulling python:3.9-slim image'
                sh 'docker pull python:3.9-slim'
            }
        }

        stage('Run Container') {
            steps {
                echo 'Running a Python container'
                sh 'docker run --rm python:3.9-slim python --version'
            }
        }
    }
}
