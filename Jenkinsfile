pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/shubhamrai028/learning_project.git', credentialsId: 'github-pat'
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

        stage('Deploy') {
            steps {
                bat 'python app.py'
            }
        }
    }
}






