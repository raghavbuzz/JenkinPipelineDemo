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
				bat 'npm install'
			}
		}
		stage ('build'){
			steps{
				bat 'npm run ng build --prod --base-href /jenkinpipelinedemo/'
			}
		}		
	}
}