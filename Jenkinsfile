//SCRIPTED
// node {
	
// 		echo "Build"
// 		echo "Test"
// 		echo "Test"	
// }

//DECLARATIVE

pipeline {
	    //agent any
		agent { 
			docker { image 'node:14.5' } 
		}
		stages {
			stage('Build') {
				steps {
					bat 'node --version'
					echo "Build"
				}		
			}
			stage('Test') {
				steps {
					echo "Test"
				}	
			}
			stage('Integration Test') {
				steps {
					echo "Integration Test"
				}
				
			}
		}
		post{
			always {
				echo 'Im awesome.I run always'
			}
			success {
				echo 'I run when you are successfull'
			}
			failure {
				echo 'I run when you fail'
			}
		}
			
}