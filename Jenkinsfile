pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Clona o repositório
                git branch: 'main', url: 'https://github.com/Newtoun/trabalhoJenkins.git'
            }
        }

        stage('Setup Python Environment') {
            steps {
                // Cria e ativa um ambiente virtual Python
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate'
            }
        }

        stage('Install dependencies') {
            steps {
                // Instala as dependências no ambiente virtual
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Executa os testes unitários no ambiente virtual
                sh '. venv/bin/activate && python -m unittest discover'
            }
        }
    }
}
