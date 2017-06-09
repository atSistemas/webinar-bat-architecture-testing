//TODO: ajustar a linux.
//TODO: configurar setting de maven para realizar el despliegue en nexus. (deploy)
//TODO: determinar la version de java(default) y la de maven.
pipeline {
    agent any
	
    stages { 		
        stage('build-and-deploy') {
            steps {
                withMaven(jdk: 'JDK_8u131', maven: 'Maven_3.5.0') {
					bat 'mvn clean install'
				}
            }
        }
    }
}