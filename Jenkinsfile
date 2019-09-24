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
				bat 'npm run ng --build --prod --baseHref=/jenkinpipelinedemo/ -optimization=true'
			}
		}
		stage ('pre-deploy'){
			steps{
				bat 'del /q "C:\\Raghav\\Codies\\Hosting\\jenkinpipelinedemo\\*"'
			}
		}		
		stage ('deploy'){			
			steps{
				bat 'xcopy dist\\Angular8POC "C:\\Raghav\\Codies\\Hosting\\jenkinpipelinedemo" /O /X /E /H /K'
			}
		}
	}
	post {
		success {
			slackSend(color: '#00FF00', message: "Build Successful")
		}
		failure {
			slackSend(color: '#FF0000', message: "Build Failed")
		}
	}
}