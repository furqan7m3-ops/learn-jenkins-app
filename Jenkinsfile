pipeline {
    agent any

    stages {
        stage('Build') {
            sh '''
            echo "Checking Node version..."
            node --version
            echo "Checking npm version..."
            npm --version
            npm run build
            '''
        }
    }
}
