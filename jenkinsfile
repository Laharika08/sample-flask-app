pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/YOUR_USERNAME/sample-flask-app.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat '"C:\\Users\\kanch\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\kanch\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pytest'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy step: Here you can add deployment commands"
                // For demo: just run the app for a short time or do nothing
            }
        }
    }
    post {
        success {
            echo '✅ Pipeline completed successfully.'
        }
        failure {
            echo '❌ Pipeline failed. Check logs.'
        }
    }
}
