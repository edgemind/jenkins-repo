//DECLARATIVE
pipeline {
	agent any

	stages{
		stage('Testttt'){
				steps{
					echo "Testing the app..."
				}
			}

	
		stage('Builddd'){
			when{
				expression{
					BRANCH_NAME == 'master'
					
				}
			}
			steps{
				echo "Building the app..."
			}
		}
		
		
		
		stage('Deploy'){
			steps{

				when {
					expression {
						BRANCH_NAME == 'master'
					}
				}


				echo "Deploying the app with ..."
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
