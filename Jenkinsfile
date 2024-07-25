pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Clona o repositório
                git branch: 'main', url: 'https://github.com/Newtoun/trabalhoJenkins.git'
            }
        }

        stage('Install dependencies') {
            steps {
                // Instala as dependências
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Executa os testes unitários
                sh 'python3 -m unittest discover'
            }
        }
    }
}
