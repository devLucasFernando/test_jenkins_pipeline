pipeline {
    agent {
        docker {
            image 'node:16'  // Use uma imagem oficial do Node.js
        }
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'  // Instala as dependências com npm
            }
        }

        stage('Release') {
            steps {
                sh 'npx standard-version'  // Executa o standard-version
            }
        }
      
        stage('Push Changes') {
            steps {
                sh 'git push --follow-tags'  // Empurra as alterações para o repositório
            }
        }
    }
}
