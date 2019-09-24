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
				bat 'npm run ng build --prod --baseHref=/jenkinpipelinedemo/ -optimization=true'
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
        always {
            echo 'One way or another, I have finished'
            deleteDir()
        }
        success {
            echo 'I succeeeded! :)'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }	
}