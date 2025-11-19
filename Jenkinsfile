pipeline {

    agent any
    
    tools {
        nodejs 'node-js24'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build Project') {
            steps {
                sh 'npm run build'
            }
        }
    }

    post {
        success {
            echo 'Go Cart Build Success'
        }
        failure {
            echo 'Go Cart Build Failed'
        }
    }
}