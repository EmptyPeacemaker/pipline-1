node {
    checkout scm
    def customImage = docker.build("pipeline-test:${env.BUILD_ID}")
//     customImage.run()
    sleep Math.abs(new Random().nextInt(10))
}