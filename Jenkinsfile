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
        stage('Core Test') {
            steps {
                echo 'Testing core...'
                sh './gradlew core:Test'
            }
        }

        stage('App Test') {
            steps {
                echo 'Testing app...'
                sh './gradlew connectedAndroidTest'
            }
        }
    }
}
