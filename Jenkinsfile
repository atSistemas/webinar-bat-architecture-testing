pipeline {
    agent any
    stages { 
		stage('info') {	
			steps {
				echo "Building branch: ${env}"
			}			
		}
		
        stage('unit-test') {
            steps {
                withMaven(jdk: 'JDK_8u131', maven: 'Maven_3.5.0') {
					bat 'mvn clean install -Pall-tests'
				}
            }
        }
		
		stage('integration-test') {
            steps {
                echo 'integration-test'
            }
        }
    }
}