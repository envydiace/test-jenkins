pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/envydiace/test-jenkins.git'
            }
        }
        stage('Clone') {
            withDockerRegistry(credentialsId: '5fb122d7-bc66-4942-bfc2-405f66502464', url: 'https://index.docker.io/v1/') {
                sh 'docker build -t envydiace/test-jenkins:v1.0.0 .'
                sh 'docker push envydiace/test-jenkins:v1.0.0 .'
            }
        }
    }
}