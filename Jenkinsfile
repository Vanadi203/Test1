pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                githubNotify context: 'jenkins-ci', status: 'FAILURE'
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
        failure {
            githubNotify context: 'jenkins-ci', status: 'FAILURE'
        }
    }
}
