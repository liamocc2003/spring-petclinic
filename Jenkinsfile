pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'

                bat '''
                    docker pull t00226053/spring-petclinic:latest
                '''
            }
        }

        stage('Run'){
            steps{
                echo 'Running...'

                bat '''
                    docker run --rm t00226053/spring-petclinic:latest
                '''
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploying...'
            }
        }
    }
}
