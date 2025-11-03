pipeline {
    agent any

	tools {
		jdk 'jdk24'
	}

    stages {
        stage ('Build') {
            steps {
                echo 'Building...'
				sh './gradlew bootJar'
            }
        }
        stage ('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}