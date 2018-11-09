pipeline{
	agent any
	tools{
		maven 'localMaven'
		jdk 'localJDK'
	}	
	stages{
		stage('Build'){
			steps{
				sh "mvn clean package"
				sh "sudo docker build . -t tomcatwebapp:${env.BUILD_ID}"
			}
		}
	}
}			 		  			
