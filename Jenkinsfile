pipeline {
	agent any
	stages {
		stage('One'){
			steps{
				echo 'Starting Build'
			}
		}		
		stage ('install modules'){
			steps{
				'C:\cygwin64\bin\sh' 'npm install'
			}
		}		
	}
}		