
pipeline {
    agent any
    environment { PATH = "C:\\WINDOWS\\SYSTEM32;C:\Users\shubham.rai\AppData\Local\Programs\Python\Python313;C:\Users\shubham.rai\AppData\Local\Programs\Python\Python313\Scripts" }
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/shubhamrai028/learning_project.git', credentialsId: 'github-pat'
            }
        }

        stage('Verify Shell') {
            steps {
                bat 'echo %SHELL%'
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

// k

