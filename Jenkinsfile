pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Deploy') {
            steps{
                echo "Deploying..."
            }
        }
    }
}
