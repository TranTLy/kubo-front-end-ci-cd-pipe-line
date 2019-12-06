pipeline{
    agent any
	
    def prefix = 'abc'

	def sourceName = prefix + '-' + 'src-master.zip'
	def sourcePath = 'D:/src'
	def sourceFullPath = sourcePath + '/' + sourceName
	
    def targetFullPath = 'D:/build/' + prefix 
	
    stages{
		stage('Prepare'){
			steps{
				bat 'git archive -v -o ' + sourceFullPath + ' HEAD'
				powershell -command 'Expand-Archive ' +  sourceFullPath + ' ' + targetFullPath
			}			 
		}
        stage('install'){
            steps{
				bat 'cd ' + targetFullPath
                bat 'npm install'
            }
        }
        stage('test'){
            steps{
				bat 'cd ' + targetFullPath
                bat 'npm run test'
            }
        }
        stage('start'){
            steps{
				bat 'cd ' + targetFullPath
                bat 'npm start'
            }
        }
    }
} 
