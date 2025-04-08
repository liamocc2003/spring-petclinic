pipeline {
    agent {
        docker {
            image "maven:3.9.9-amazoncorretto-17-debian"
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'

                bat '''
                    mvn --version
                '''
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
