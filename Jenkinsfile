pipeline {
    agent any

    stages {
        stage('clonar repositorio') {
            steps {
               git branch: 'main', url: 'https://github.com/oqvine/teste-web-jenkinsfile'
            }
        }
        stage('Instalar dependencias') {
            steps {
               bat 'npm install'
            }
        }
        stage('Excecutar testes') {
            steps {
               bat 'npm run cy:run'
            }
        }
    }
}
