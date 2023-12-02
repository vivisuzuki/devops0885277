pipeline {
    agent any
    stages {
        stage('Verificação Ferramentas') {
            steps {
                sh '''
                docker info
                docker version
                docker-compose version
                java --version
                '''
            }
        }
        stage('Instalação Dependências') {
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
        stage('Up') {
            steps {
                sh 'docker-compose up'
            }
        }
    }
}
