pipeline {
    agent {
        docker {
            image 'devops-server:latest'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'

                bat '''
                    mvn --version
                '''
                bat '''
                    docker build -t t00226053/devops-server:latest .
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
