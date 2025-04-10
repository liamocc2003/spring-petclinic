pipeline {
    agent any

    environment {
	    IMAGE = 't00226053/spring-petclinic:latest'
	    CONTAINER = 'petclinic'
	    SONAR_TOKEN = 'squ_9c9b469a9034d2cabb81526ae96b0268b5f906f7'
    }

    stages {
	    stage('Testing') {
	        steps {
	    	    echo 'Testing...'

	    	    script {
                    withSonarQubeEnv('sonar') {
                        bat '''
                            cd ../../tools/hudson.plugins.sonar.SonarRunnerInstallation/sonarqube_scanner/bin

                            sonar-scanner -Dsonar.projectKey=spring-petclinic
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
                    docker stop %CONTAINER%
                    docker rm %CONTAINER%
                    docker run -p 8080:8080 -d --name %CONTAINER% %IMAGE%
                '''
            }
        }
    }

    post {
        always {
            emailext (
                subject: "Jenkins Test Email",
                body: "Test",
                to: "liam.oconnor-collum@students.ittralee.ie"
            )
        }
    }
}
