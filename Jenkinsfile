pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Shyamsundaryadav23/devops-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Running basic verification...'
                bat 'if exist app.py (echo app.py found) else (exit /b 1)'
            }
        }
    }

    post {
        success {
            echo 'Jenkins GitHub integration completed successfully.'
        }
        failure {
            echo 'The pipeline failed. Check the console output.'
        }
    }
}
