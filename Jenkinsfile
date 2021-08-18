pipeline {
    environment {
        registry = "maurivg25/maurirepo"
        registryCredential = 'dockerHub'
    }
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/maurivg28/votingapp.git'
            }
        }
    }
        stage('Build Image') {
            steps {
                script {
                    dockerImage = docker.build registry + ":$BUILD_NUMBER"
                }
            }
        }
}