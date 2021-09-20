//DECLARATIVE
pipeline {
	agent any
	environment{
		NEW_VER = '1.2'
		NEW_CRED = credentials("git-cred")
	}
	stages{
		stage('Buildddd'){
			when{
				expression{
					BRANCH_NAME == 'dev'
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
				echo "testing with ${NEW_CRED}"
			}
		}
		stage('Deploy'){
			steps{
				echo "Deploying with ..."
				withCredentials(
					[
						usernamePassword(credentials: 'git-cred', usernameVariable: USER, passwordVariable: PWD)
					]
					sh "some script with user pass variables: ${USER} , ${PWD}"
				)
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
