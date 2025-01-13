pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/shubhamrai028/learning_project.git', credentialsId: '92c7363c-b502-4872-aa61-2b5dd2669a7b'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        
        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my_flask_app .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 5000:5000 my_flask_app'
            }
        }
    }
}
