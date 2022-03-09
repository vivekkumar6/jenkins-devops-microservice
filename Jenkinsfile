pipeline {
	agent any
	stages {
		stage("Build") {
			steps {
				echo "This is build stage"
				echo "$PATH"
				echo "$env.BUILD_NUMBER"
				echo "$env.BUILD_ID"
				echo "$env.JOB_NAME"
				echo "$env.BUILD_TAG"
				echo "$env.BUILD_URL"
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
