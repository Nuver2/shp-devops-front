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
    }
    stage('Production') {
    steps {
        script {
            docker.image('node:latest').inside {
                sh 'npm run build'
            }
        }
    }
}
}
