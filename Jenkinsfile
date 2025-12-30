pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                echo "Checking Node version..."
                node --version
                echo "Checking npm version..."
                npm --version
                npm run build
                '''
            }
            
        }
    }
}
