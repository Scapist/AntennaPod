pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh './gradlew assembleDebug'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                echo 'Testing...'
            }
        }
    }
}
