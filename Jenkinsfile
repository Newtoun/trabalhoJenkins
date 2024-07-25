pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Clona o repositório
                git 'https://github.com/Newtoun/trabalhoJenkins.git'
            }
        }

        stage('Install dependencies') {
            steps {
                // Instala as dependências
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Executa os testes unitários
                sh 'python -m unittest discover'
            }
        }
    }
}
