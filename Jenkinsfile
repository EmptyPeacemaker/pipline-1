node {
    checkout scm
    docker.withRegistry('https://registry.expertcentre.org', 'docker-hub') {
        def customImage = docker.build("pipeline-test:${env.BUILD_ID}")
        customImage.push()
        customImage.push('latest')
    }
}