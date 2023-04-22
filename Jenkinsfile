node{
    withDockerContainer(args: '-p 3030:3030' , image: 'node:16-buster-slim' )
    stage('Build'){
        sh 'npm cache clean --force'
        sh 'npm install --legacy-peer-deps'
    }
    stage('Tests'){
        sh './jenkins/scripts/test.sh'
    }
}