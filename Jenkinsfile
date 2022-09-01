node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
         USER root
         sh 'RUN curl -fsSLO https://get.docker.com/builds/Linux/x86_64/docker-17.04.0-ce.tgz \
                && tar xzvf docker-17.04.0-ce.tgz \
                && mv docker/docker /usr/local/bin \
                && rm -r docker docker-17.04.0-ce.tgz'
        app = docker.build("releaseworks/hellonode")
    }
}
