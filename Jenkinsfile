pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                checkout scm
            }
        }
    }
    stages{
        stage('test'){
            steps{
                sh 'sudo apt install npm'
                sh 'npm test'
            }
        }
    }
    stages{
        stage('Build'){
            steps{
                sh 'npm run build'
            }
        }
    }

}