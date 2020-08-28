pipeline {
    agent any
    tools {
        maven 'Maven 3'
        jdk 'JDK 1.8'
    }
	
    stages {
        stage('Initialize') {
            steps {
                cmd '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
        stage('Build') {
            steps {
                cmd 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}