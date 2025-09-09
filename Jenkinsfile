pipeline {
    agent any
    environment {
        FIREBASE_TOKEN = credentials('FirebaseToken')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Build stage...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Staging') {
            steps {
                echo 'Preparing for production...'
            }
        }
        stage('Production') {
            steps {
                sh 'firebase deploy --token "$FIREBASE_TOKEN"'
            }
        }
    }
}
