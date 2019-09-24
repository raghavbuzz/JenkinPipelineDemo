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
				bat 'npm run ng build --prod'
			}
		}		
		stage ('deploy'){
			steps{
				bat 'xcopy dist\\Angular8POC "C:\\Raghav\\Codies\\Hosting\\jenkindemo" /O /X /E /H /K'
			}
		}
	}
}