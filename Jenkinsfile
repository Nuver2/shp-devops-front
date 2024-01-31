pipeline {
    agent {
        docker { image 'node:latest' }
    }
    stages {
        stage('Установка зависимостей') {
            steps {
                sh 'npm install'
            }
        }
    }
}
