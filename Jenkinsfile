pipeline {
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    docker.image('node:latest').inside {
                        sh 'npm install'
                    }
                }
            }
        }
    }
}
