node{
    docker.image('node:16-buster-slim').inside('-p 3000:3000'){
        stage('Build'){
            sh 'npm install --legacy-peer-deps'
        }
        stage('Tests'){
            sh './jenkins/scripts/test.sh'
        }
    }
}