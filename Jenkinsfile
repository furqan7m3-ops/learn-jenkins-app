pipeline {
    agent any

    stages {
        stage('Build in Docker') {
            steps {
                bat '''
                docker run --rm ^
                --user root ^
                -v "%cd%:/app" ^
                -w /app ^
                node:18-alpine ^
                sh -c "npm install && npm run build"
                '''

            }
        }
    }
}
