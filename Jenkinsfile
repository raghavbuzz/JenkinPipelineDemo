pipeline {
	agent any
	stages {
		stage('One'){
			steps {
				echo 'Hi from 1st Step'
			}
		}
		stage('git clone'){
			steps {
				git clone "https://github.com/raghavbuzz/JenkinPipelineDemo.git"
			}
		}
	}
}