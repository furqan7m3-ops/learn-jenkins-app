pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                @echo on
                echo "Checking Node version..."
                node --version
                echo "Checking npm version..."
                npm --version
                echo "Installing Dependencies"
                call npm install
                echo "Building..."
                call npm run build
                '''
            }
            
        }
    }
}
