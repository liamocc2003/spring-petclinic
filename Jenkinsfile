pipeline {
    agent any

    environment {
	    IMAGE = 't00226053/spring-petclinic:latest'
    }

    stages {
	    stage('Testing') {
	        steps {
	    	    echo 'Testing...'

	    	    script {
	    	        def scanner_home = tool name: 'sonarqube_scanner', type: 'hudson.plugins.sonar.sonarRunnerInstallation'
                    withSonarQubeEnv('sonar') {
                        bat '''
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
