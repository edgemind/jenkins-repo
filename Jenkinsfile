//DECLARATIVE
pipeline {
	agent any
	
	
	
	stages{
		stage('Buildddd'){
			steps{
				echo "Builddddd"
			}
		}
		stage('Pre-test'){
			steps{
				echo "pretest..."
			}
		}
		
		stage('Testttt'){
			steps{
				echo "testtt"
			}
		}
		stage('Integggg'){
			steps{
				echo "Integgg"
			}
		}
	}
	post{
		always{
			echo 'ALWAYSSS'
		}
		success{
			echo 'SUCCESSFULLL'
		}
		failure{
			echo 'FAILEDDD'
		}
	}
}
