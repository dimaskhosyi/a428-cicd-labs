pipeline {
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 3040:3040' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm cache clean --force'
                sh 'npm install --legacy-peer-deps' 
            }
        }
    }
}
