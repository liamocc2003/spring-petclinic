pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat 'docker build -t t00226053/devops-server:latest .'
            }
        }

        stage('Run'){
            steps{
                echo 'Running...'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploying...'
            }
        }
    }
}
