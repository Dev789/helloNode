node {
    def app
    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    agent {
        label 'docker'
    }
    stage('Build image') {
        sh 'docker build --tag django-pipeline .'
    }
}
