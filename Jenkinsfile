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
        failure {
            setGitHubPullRequestStatus state: 'FAILURE'
        }
    }
}
