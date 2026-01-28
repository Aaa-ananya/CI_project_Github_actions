pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/<your-username>/github-actions-learning.git'
            }
        }

        stage('Build & Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Build & Tests passed 🎉'
        }
        failure {
            echo 'Build or Tests failed ❌'
        }
    }
}
