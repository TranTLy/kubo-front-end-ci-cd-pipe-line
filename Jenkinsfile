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
                bat 'npm test -- --no-watch'
            }
        }
        stage('start'){
            steps{
                bat 'npm start'
            }
        }
    }
} 
