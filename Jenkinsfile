node {
    checkout scm
    docker.withRegistry('registry.expertcentre.org', 'docker-hub') {
        def customImage = docker.build("pipeline-test:${env.BUILD_ID}")
        customImage.push()
        customImage.push('latest')
//         docker.image('mysql:8-oracle').withRun('-p 3306:3306') {
//             /* do things */
//         }
    }




}