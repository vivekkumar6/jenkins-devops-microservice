pipeline {
	agent {
		docker {image 'node:16.13.1-alpine'}
	}
	stages {
		stage("Build") {
			steps {
				sh 'node --version'
				echo "This is build stage"
			}
		}
		stage("Test") {
			steps{
				echo "This is test stage"
			}
		}		
	} 
	post {
		always {
			echo 'I run always'
		}
		success {
			echo 'I run if its successful'
		}
		failure {
			echo 'I run if its a failure'
		}
	}
}
