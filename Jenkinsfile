pipeline {
    agent any
    triggers {
        githubPush()
    }
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
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
