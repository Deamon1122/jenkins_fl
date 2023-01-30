pipeline {
    agent any
	
	tools {
	    maven "Apache Maven 3.8.7"  
	}
	
	stages {
	    stage('Git clone') {
	        steps {
            git credentialsId: '9104106104a@gmail.com', url:'https://github.com/Deamon1122/Asweb.git'
            }
		    }
        stage('MVN version') {
	        steps {
            sh 'mvn --version'
            }
			}
        stage('mvn Clean') {
	        steps {
            sh 'mvn clean'
			}
			}
		stage('MVN Validate') {
	        steps {
            sh 'mvn validate'
            }
			}
        stage('mvn Compile') {
	        steps {
            sh 'mvn compile'
			}
			}
		stage('MVN Test') {
	        steps {
            sh 'mvn test'
            }
			}	
		stage('MVN Package') {
	        steps {
            sh 'mvn package'
            }
			}		
		stage('MVN Deploy') {
	        steps {
            sh 'mvn deploy'
			}
			}
		}	
}		