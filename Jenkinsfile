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
                powershell 'npm install --save-dev start-server-and-test
'
               
                
            }
        }
        
          stage('Instalar servidor') {
            steps {
                powershell 'cy:run-cy': 'start-server-and-test start http://localhost:3000/usuarios test'
               
                
            }
        }
        
         stage('Executar testes') {
            steps {
              powershell 'npm run cy:run'
                
            }
        }
    }
}
