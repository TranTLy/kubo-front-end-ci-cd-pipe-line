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
        stage('build'){
            steps{
                bat 'npm run build'
            }
        }
         stage('serve'){
            steps{
                bat 'serve -s build'
            }
        }
        stage('start'){
            steps{
                bat 'npm start'
            }
        }
    }
} 
