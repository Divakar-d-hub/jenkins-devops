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
	// agent { docker { image 'maven:3.9.9' } }
	agent any
	environment{
		dockerhome= tool "mydocker"
		mavenhome= tool "mymaven"
		PATH= "$dockerhome/bin:$mavenhome/bin:$PATH"
	}
	stages{
		stage('checkout'){	
			steps{
				sh "mvn --version"	
				sh "docker version"
				echo "PATH - $PATH"
				echo "BUILD_ID- $env.BUILD_ID"
				echo "BUILD_URL- $env.BUILD_URL"
				echo "JOB_NAME- $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
			}
		}
		stage('Build'){
			steps{
				sh "mvn clean compile"
			}
		}
		stage('Test'){
			steps{
		        sh "mvn test"
			}
		}
		stage('Integration Test'){
			steps{
		        sh "mvn failsafe:integration-test failsafe:verify"
			}
		}
	}
	// post
	// {
	// 	always{
	// 		echo 'run always'
	// 	}
	// 	success{
	// 		echo 'run when success'
	// 	}
	// 	failure
	// 	{
	// 		echo 'run when failure'
	// 	}
	// }
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
