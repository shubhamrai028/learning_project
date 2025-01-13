pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/shubhamrai028/learning_project.git', credentialsId: 'github-pat'
            }
        }
        
        stage('Verify Environment') {
            steps {
                bat 'python --version'
                bat 'pip --version'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        
        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my_flask_app .'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker run -d -p 5000:5000 my_flask_app'
            }
        }
    }
}
