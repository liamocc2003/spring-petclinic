pipeline {
    agent any

    environment {
	    IMAGE = 't00226053/spring-petclinic:latest'
	    SONAR_SECRET = 'squ_9c9b469a9034d2cabb81526ae96b0268b5f906f7'
    }

    stages {
	    stage('Testing') {
	        steps {
	    	    echo 'Testing...'

	    	    script {
	    	        def scanner_home = tool name: 'sonarqube_scanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
                    withSonarQubeEnv('sonar') {
                        bat '''
                            echo %scanner_home%
                            %scanner_home%/bin/sonarqube-scanner
                        '''
                    }
	    	    }
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
            steps {
                echo 'Running...'

                bat '''
                    docker run -p 8080:8080 --rm %IMAGE%
                '''
            }
        }
    }
}
