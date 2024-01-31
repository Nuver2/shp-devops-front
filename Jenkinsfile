pipeline {
    agent {
        docker { image 'node:latest' }
    }
    stages {
        stage('Установка зависимости') {
            steps {
                sh 'npm install'
            }
        }
        stage('production') {
            steps {
                sh 'npm run build:production'
            }
        }
    }
}
