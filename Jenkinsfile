pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                docker run --rm -v "%cd%:/app" -w /app node:18-alpine sh -c npm install && npm run build
                '''
            }
            
        }
    }
}
