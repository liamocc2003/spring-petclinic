pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'

                sh '''
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
