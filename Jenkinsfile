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
				sh 'ng build --prod --base-href /jenkinpipelinedemo/'
			}
		}		
	}
}