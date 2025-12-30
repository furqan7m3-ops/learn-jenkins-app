pipeline {
    agent any

    stages {
        stage('Build in Docker') {
            steps {
                bat "docker run -d -v %cd%:/app --name build-node-app node:18-alpine bash"
                bat "docker exec build-node-app npm install"
                bat "docker exec build-node-app npm run build"
            }
        }
    }
}
