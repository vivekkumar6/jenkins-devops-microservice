pipeline {
	agent { 
		docker { image 'node:13.8'}
	}
	stages {
		stage("Build") {
			steps {
				sh 'node --version'
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
