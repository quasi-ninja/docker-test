pipeline {
    agent { dockerfile true }
    stages {
        stage('Preparation') {
            git 'https://github.com/quasi-ninja/docker-test.git'
        }
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }
}