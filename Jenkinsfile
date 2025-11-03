pipeline {
	agent any

	tools {
		jdk 'jdk21'
	}

	stages {
		stage('Build') {
			steps {
				echo 'Checking Java version...'
				sh 'java -version'

				echo 'Building...'
				sh './gradlew bootJar'
			}
		}

		stage('Deploy') {
			steps {
				echo 'Deploying...'
			}
		}
	}
}
