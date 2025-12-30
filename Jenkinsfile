pipeline {
    agent any

    stages {
        stage('W/O Docker') {
            steps {
                echo 'Without Docker'
            }
        }
        stage('Hello') {
            steps {
                script {
                    // Get workspace path in WSL format
                    def workspace = pwd()
                    
                    // Run with volume mount
                    bat "docker run --rm -v \"${workspace}:/app\" -w /app node:18-alpine node --version"
                    bat "docker run --rm -v \"${workspace}:/app\" -w /app node:18-alpine npm --version"
                }
            }
    }
    }
}
