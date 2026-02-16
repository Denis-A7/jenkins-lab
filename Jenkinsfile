pipeline {
    agent any

    tools {
        jdk 'JDK21'
    }

    stages {

        stage('Build') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java Hello'
            }
        }
    }
}
