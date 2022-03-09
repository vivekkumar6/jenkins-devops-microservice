pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage("Checkout") {
			steps {
				echo "This is the checkout stage"
				sh 'mvn --version'
				sh 'docker version'
			}
		}
		stage("Compile") {
			steps {
				sh "mvn clean compile"
			}
		}
		stage("Test") {
			steps {
				sh "mvn test"
			}
		stage("Integration Test") {
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
			}
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
