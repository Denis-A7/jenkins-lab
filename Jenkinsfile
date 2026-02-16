pipeline {
    agent any

    tools {
        jdk 'Java17'   // Must match Jenkins Global Tool name
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Denis-A7/jenkins-lab.git'
            }
        }

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

    post {
        success {
            archiveArtifacts artifacts: '*.class', fingerprint: true
            echo 'Build Successful! Artifact Archived.'
        }

        failure {
            echo 'Build Failed!'
        }
    }
}
