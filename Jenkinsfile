//DECLARATIVE
pipeline {
	//agent any
	agent { docker {image 'maven:3.6.3'} }
	stages{
		stage('Buildddd'){
			steps{
				echo "Builddddd"
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
