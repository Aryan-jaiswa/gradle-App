pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/YOUR_USERNAME/Gradle-Jenkins-App.git'
            }
        }
        stage('Check Gradle Version') {
            steps { sh 'gradle -version' }
        }
        stage('Build Project') {
            steps { sh 'gradle build' }
        }
        stage('Run Tests') {
            steps { sh 'gradle test' }
        }
        stage('Run Application') {
            steps { sh 'gradle run' }
        }
        stage('Custom Task') {
            steps { sh 'gradle display' }
        }
        stage('Custom Message') {
            steps {
                echo 'Gradle Jenkins Pipeline Executed Successfully!'
            }
        }
    }
    post {
        success { echo 'BUILD SUCCESSFUL'             }
        failure { echo 'BUILD FAILED'                 }
        always  { echo 'Pipeline execution finished.' }
    }
}
