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
        stage('instalação dependências') {
            steps {
                sh 'npm install'
            }
       }
       stage('Testes') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'docker-compose build'
            }
        }
    }
}
