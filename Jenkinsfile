pipeline {
    agent any
    stages {
        stage('verificação ferramentas') {
            steps {
                sh '''
                docker info
                docker version
                docker-compose version
                java --version
                '''
            }
        }
    }
    stages {
        stage('instalação dependências') {
            steps {
                sh 'npm install'
            }
        }
    }
}
