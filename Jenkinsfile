pipeline {
    agent any

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