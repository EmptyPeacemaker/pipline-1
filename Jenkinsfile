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
node {
		stage (‘Build’) {
			bat "msbuild ${C:\\Jenkins\\my_project\\workspace\\test\\my_project.sln}"
		}

    stage('Selenium tests') {
        dir(automation_path) {  //changes the path to “automation_path”
            bat "mvn clean test -Dsuite=SMOKE_TEST -Denvironment=QA"
        }
    }
}