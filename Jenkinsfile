pipeline {
    agent {
        docker {
            image 'devops-server:latest'
            label 'Docker'
        }
    }

    tools {
        maven "3.9.9"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn --version'
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
