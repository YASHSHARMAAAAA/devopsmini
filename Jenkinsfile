pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
        stage('Docker Build') {
            steps {
                script {
                    bat "docker build -t devopsminiproject ."
                }
            }
        }
    }
}
