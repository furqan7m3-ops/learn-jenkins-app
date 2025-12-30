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
                echo "Installing Dependencies"
                npm install
                echo "Building..."
                npm run build
                '''
            }
            
        }
    }
}
