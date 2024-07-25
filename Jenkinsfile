pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Clona o repositório
                git 'https://seu-repositorio.git'
            }
        }

        stage('Install dependencies') {
            steps {
                // Instala as dependências
                sh 'pip install -r requeriment.txt'
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
