node {
    // def app
    agent any
    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    agent {
        label 'docker-agent'
    }
    stage('Build image') {
        sh 'docker build --tag django-pipeline .'
    }
}
