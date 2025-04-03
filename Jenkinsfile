pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'make build'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }

        stage('Deploy') {
            steps{
                echo "Deploying..."
            }
        }
    }
}
