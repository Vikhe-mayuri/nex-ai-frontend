pipeline {
    agent any

    stages {
        stage('Clone Frontend') {
            steps {
                echo 'Cloned by Jenkins automatically.'
            }
        }

        stage('Install & Build Frontend') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }

        stage('Clone Backend') {
            steps {
                git url: 'https://github.com/Vikhe-mayuri/nex-ai-backend.git', branch: 'main'
            }
        }

        stage('Install Backend Requirements') {
            steps {
                dir('nex-ai-backend') {
                    sh 'pip install -r requirements.txt'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step goes here.'
            }
        }
    }
}
