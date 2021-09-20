//DECLARATIVE
pipeline {
	agent any

	parameters{
		booleanParam(name: 'exec-test', defaultValue: true, description: 'nothing to desc')
		choice(name: 'VERSION', choices: ['1.1', '1.2', '1.3'], description: 'nothing to desc')
	}

	stages{
		stage('Builddd'){
			when{
				expression{
					params.exec-test
					
				}
			}
			steps{
				echo "Building ver got from var is: ${params.VERSION}"
			}
		}
		
		
		stage('Testttt'){
			steps{
				echo "Value of env var at test ${params.exec-test}"
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
