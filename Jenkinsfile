pipeline {
    agent any

    stages {
        stage('Git Scm') {
            steps {
                echo 'Cloning git repo'
                git branch: 'main', url: 'https://github.com/Vikhe-mayuri/nex-ai-frontend.git'
            }
        }
        stage('Installing npm') {
            steps {
                echo 'Installing npm'
                sh '''npm install
                '''
            }
        }
        stage('Starting npm') {
            steps {
                echo 'Starting npm'
                sh '''npm start
                '''
            }
        }
    }
}
