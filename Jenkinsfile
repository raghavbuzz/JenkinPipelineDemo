pipeline {
	agent any
	stages {
		stage('One'){
			steps{
				echo 'Starting Build'
			}
		}
		stage('checkout'){
			steps{
				checkout scm
			}
		}
		stage ('install modules'){
			steps{
				sh 'npm install'
			}
		}		
	}
}		