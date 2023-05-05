node {
    checkout scm
    def customImage = docker.build("pipeline-test:${env.BUILD_ID}")
    customImage.push()
    customImage.push('latest')
}