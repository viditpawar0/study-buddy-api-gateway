pipeline {
	agent any

	tools {
		jdk 'jdk21'
		DockerTool
	}

	stages {
		stage('Build') {
			steps {
				script {
					echo 'Building...'

					echo 'Building Jar file...'
					sh './gradlew bootJar'
					echo 'Jar build completed successfully'

					echo 'Building Docker image...'
					image = docker.build('viditpawar/study-buddy-api-gateway')
					echo 'Docker image build completed successfully'
				}
			}
		}

		stage('Deploy') {
			steps {
				echo 'Deploying...'

				echo 'Pushing Docker image to Docker Hub...'
				sh 'docker push viditpawar/study-buddy-api-gateway'
				echo 'Docker image pushed to Docker Hub successfully'
			}
		}
	}
}
