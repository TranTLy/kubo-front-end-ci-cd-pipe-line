pipeline{
    agent any
    stages{
        stage('install'){
            steps{
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                sh 'npm run test'
            }
        }
        stage('start'){
            steps{
                sh 'npm start'
            }
        }
    }
} 
