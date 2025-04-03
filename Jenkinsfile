pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './mvnw sprint-boot:run'
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
