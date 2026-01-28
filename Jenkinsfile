pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Aaa-ananya/CI_project_Github_actions'
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
