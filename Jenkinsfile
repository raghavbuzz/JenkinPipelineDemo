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
				sh 'npm install'
			}
		}
		stage ('build'){
			steps{
				sh 'npm run ng build --prod'
			}
		}		
	}
}