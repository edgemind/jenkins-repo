//DECLARATIVE
pipeline {
	agent any

	parameters{
		booleanParam(name: 'execTest', defaultValue: true, description: 'nothing to desc')
		choice(name: 'VERSION', choices: ['1.1', '1.2', '1.3'], description: 'nothing to desc')
	}

	stages{
		stage('Builddd'){
			when{
				expression{
					params.execTest
					
				}
			}
			steps{
				echo "Building ver got from var is: ${params.VERSION}"
			}
		}
		
		
		stage('Testttt'){
			steps{
				echo "Value of exec params ${params.execTest}"
			}
		}
		stage('Deploy'){
			steps{
				echo "Deploying with ..."
				//withCredentials(
				//	[
				//		usernamePassword(credentials: 'git-cred', usernameVariable: USER, passwordVariable: PWD)
				//	]
					//echo "some script with user pass ${USER}"
				//)
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
