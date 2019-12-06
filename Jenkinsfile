pipeline{
    agent any
    stages{
        stage('install'){
            steps{
                bat 'npm install'
            }
        }
        stage('test'){
            steps{
                bat 'npm run coverage'
            }
        }
        stage('start'){
            steps{
                bat 'npm start'
            }
        }
    }
} 
