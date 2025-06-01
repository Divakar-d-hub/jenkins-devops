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
		stage('build'){	
			steps{
				sh "mvn --version"	
				sh "docker version"
				echo "$PATH"
				echo "env.BUILD_ID"
				echo "env. BUILD_URL"
				echo "env.JOB_NAME"
				echo "env.BUILD_TAG"
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
