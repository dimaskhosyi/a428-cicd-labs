node{
    docker.image('node:16-buster-slim').inside('-p 3130:3130'){
        stage('Build'){
            sh 'npm cache clean --force'
            sh 'curl  https://www.google.com'
            sh 'npm install --legacy-peer-deps'
        }
        stage('Tests'){
            sh './jenkins/scripts/test.sh'
        }
    }
}