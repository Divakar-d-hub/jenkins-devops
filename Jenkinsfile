// //scripted
// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"
// }

// declarative
pipeline
{	
	//agent any
	agent {docker {image {maven:3.6.3} } }
	stages{
		stage('build'){
			steps{
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test'){
			steps{
		        echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
		        echo "Integration Test"
			}
		}
	}
	post
	{
		always{
			echo 'run always'
		}
		success{
			echo 'run when success'
		}
		failure
		{
			echo 'run when failure'
		}
	}
}




// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Integration Test"
// 	}
// }
