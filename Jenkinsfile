node {
    // def app
    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
        // git credentialsId: '268c95c8-dfc1-4c35-b4d3-ec6c2cf8d71a', url: 'https://github.com/Dev789/helloNode.git'
        // sh 'ls -lart'
        // sh "git branch -a"
        // sh "git checkout main"
    }
    agent {
        dockerfile true
    }
    stage('Build image') {
        sh 'ls -l'
        sh 'docker build --tag django-pipeline .'
    }
}
