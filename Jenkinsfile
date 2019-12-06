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
        stage('start'){
            steps{
                bat 'serve -s build'
            }
        }
    }
} 
