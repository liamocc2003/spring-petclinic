pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './mvnw spring-boot:run'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploying...'
            }
        }
    }
}
