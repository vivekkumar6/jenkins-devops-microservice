pipeline {
	stages {
		stage("Build") {
			steps {
				echo "Build"
			}
		}
		stage("Test") {
			steps{
				echo "Test"
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
