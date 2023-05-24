pipeline {
    agent any

    stages {
        stage('Clonar o respositório') {
            steps {
                git branch: 'main', url: 'https://github.com/camilaigarcias/aula-jenkins.git'
                
            }
        }
         stage('Instalar dependências') {
            steps {
                bat 'npm install'
   
                
            }
        }
         stage('Instalar dependências') {
            steps {
                bat 'npm start'
   
                
            }
        }
         stage('Executar testes') {
            steps {
              powershell 'npm run cy:run'
                
            }
        }
    }
}
