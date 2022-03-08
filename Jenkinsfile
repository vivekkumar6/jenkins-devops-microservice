pipeline {
	agent {
		docker {image 'maven:3.6.3'}
	}
	stages {
		stage("Build") {
			steps {
				sh 'mvn --version'
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
