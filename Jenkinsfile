pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'docker build -t t00226053/spring-petclinic .'
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
