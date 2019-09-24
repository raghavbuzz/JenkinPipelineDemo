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
				sh 'npm run build-prod'
			}
		}		
	}
	post {
        always {
            echo 'One way or another, I have finished'
            deleteDir()
			dir("${workspace}@tmp") {
                deleteDir()
            }            
            dir("${workspace}@script") {
                deleteDir()
            }
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