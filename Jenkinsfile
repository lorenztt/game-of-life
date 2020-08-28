pipeline {
    agent any
    tools {
        maven 'Maven 3'
        jdk 'JDK 1.8'
    }
	
    stages {
        stage('Initialize') {
            steps {
                bat '''
                    echo "PATH = %PATH%"
                    echo "M2_HOME = %M2_HOME%"
                '''
            }
        }
        stage('Build') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'mvn install'
            }
        }
		stage('Promote') {
			steps {
				def userInput = input(
					id: 'userInput', message: 'Let\'s promote?')

					if(userInput == true) {
					echo "DEPLOY HORS PROD"
					} else {
					echo "Action was aborted."
					}
				}    
			}  
		}
    }
}