pipeline {
    agent any

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
