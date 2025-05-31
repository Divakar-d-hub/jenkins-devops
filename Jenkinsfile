// //scripted
// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"
// }

// declarative
pipeline
{	
	agent any
	stages{
		stage('build'){
			steps{
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
