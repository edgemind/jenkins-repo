//DECLARATIVE
pipeline {
	agent any

	parameters{
		booleanParam(name: 'exec-test', defaultValue: true)
		choice(name: 'VER', choices: ['1.1', '1.2', '1.3'])
	}


	environment{
		NEW_VER = '5.5'
		//NEW_CRED = credentials("git-cred")
	}
	stages{
		stage('Builddd'){
			when{
				expression{
					params.exec-test
					
				}
			}
			steps{
				echo "Building ver got from var is: ${NEW_VER}"
			}
		}
		stage('Pre-test'){
			steps{
				echo "pretest..."
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
