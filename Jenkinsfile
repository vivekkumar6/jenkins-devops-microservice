pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage("Build") {
			steps {
				echo "This is build stage"
				sh 'mvn --version'
				sh 'docker version'
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
