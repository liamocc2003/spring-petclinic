pipeline {
    agent any

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
                    docker pull t00226053/spring-petclinic:latest
                '''
            }
        }

        stage('Run') {
            steps{
                echo 'Running...'

                bat '''
                    docker run -p 8080:8080 --rm t00226053/spring-petclinic:latest
                '''
            }
        }
    }
}
