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
         stage('на production') {
            steps {
                sh "scp -r dist/* user@production_server:${env.SERVER_PROJECT_PATH}" 
            }
        }
    }
}

