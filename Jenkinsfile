pipeline {
    agent any

    environment {
	    IMAGE = 't00226053/spring-petclinic:latest'
    }

    stages {
	    stage('Testing') {
	        steps {
	    	    echo 'Testing...'
	        }
	    }

        stage('Build') {
            steps {
                echo 'Building...'

                bat '''
                    docker pull %IMAGE%
                '''
            }
        }

        stage('Run') {
            steps{
                echo 'Running...'

                bat '''
                    docker run -p 8080:8080 --rm %IMAGE%
                '''
            }
        }
    }
}
