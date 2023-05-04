pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                def customImage = docker.build("pipeline-test:${env.BUILD_ID}")
//                 customImage.push('latest')
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "dir ${env.WORKSPACE}"
            }
        }
    }
}