pipeline{
	stages{
		stage('Build'){
			echo 'Build'
		}
		stage('Test'){
			echo 'Test'
		}
		
	} post{
		always{
			echo 'I run always'
		}
		success{
			echo 'I run if its succesful'
		}
		failure{
			echo 'I run if its a failure'
		}
	}
}
