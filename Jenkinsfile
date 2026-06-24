pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Jenkinsfile is working!'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post {
        success {
             githubNotify context: 'jenkins-ci', status: 'SUCCESS'
        }
        failure {
             githubNotify context: 'jenkins-ci', status: 'FAILURE'
        }
    }
}
