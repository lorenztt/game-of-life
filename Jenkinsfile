pipeline {
    agent any
    tools {
        maven 'Maven 3'
        jdk 'JDK 1.8'
    }
	
    stages {
        stage('Initialize') {
            steps {
                echo 'Initialize..'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn compile'
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