pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './mvnw compile'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploying...'
            }
        }
    }
}
