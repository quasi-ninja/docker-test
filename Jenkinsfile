pipeline {
    agent { dockerfile true }
    stages {
        stage('Preparation') {
           def dockerHome = tool 'docker'
           env.PATH = "${dockerhome}/bin:${dockerhome}/bin:${env.PATH}" 
           steps {
              git 'https://github.com/quasi-ninja/docker-test.git'
           }
        }
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }
}
