pipeline {
    agent any
    environment { PATH = "C:\\WINDOWS\\SYSTEM32" }
    stages {
        stage('Print PATH') {
            steps {
                bat 'echo %PATH%'
            }
        }
        stage('Verify Shell') {
            steps {
                bat 'cmd /c echo CMD is available'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'your-command-here'
            }
        }
    }
}


// pipeline {
//     agent any

//     stages {
//         stage('Clone Repository') {
//             steps {
//                 git url: 'https://github.com/shubhamrai028/learning_project.git', credentialsId: 'github-pat'
//             }
//         }

//         stage('Verify Shell') {
//             steps {
//                 bat 'echo %SHELL%'
//             }
//         }


//         stage('Install Dependencies') {
//             steps {
//                 bat 'pip install -r requirements.txt'
//             }
//         }
        
//         stage('Run Tests') {
//             steps {
//                 bat 'pytest'
//             }
//         }

//         stage('Deploy') {
//             steps {
//                 bat 'python app.py'
//             }
//         }
//     }
// }



