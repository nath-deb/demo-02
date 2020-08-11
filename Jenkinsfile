pipeline {
	agent any 
		stages { 
			stage('Bitbucket') {
				steps {
					echo '********* SCM stage is starting **********'
					}
				}
			stage('SonarQube Analyze') {
				steps {
					echo '********* SonarQube Analyzing Starting************'
					}
				}
			stage('Veracode Application Security Check') {
				steps {
					echo '*********Application Scan Started*********'
					}
				}
			stage('Select Proceed For Final Build') {
				steps {
					input('Want to proceed the build or abort?')
				}
				}
			stage('MSBuild') {
				steps {
					echo '**********Application Build Stating **********'
					}
				}
			stage('Artifact Creation') {
				steps {
					echo 'Creating and storing Artifact in Nexus'
					}
				}
			stage('Deployment on AWS') {
				steps {
					echo 'Terraform Script will run for the AWS Deployments'
					}
				}
			}
}
