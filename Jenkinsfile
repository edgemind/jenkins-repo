//DECLARATIVE
pipeline {
	agent any
	stages{
		stage('Buildddd'){
			when{
				expression{
					BRANCH_NAME == 'dev'
				}
			}
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
