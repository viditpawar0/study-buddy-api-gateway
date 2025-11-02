pipeline {
    agent any

	tools {
		jdk 'JDK24'
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