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
            echo "Build passed! Commit is good."
        }
        failure {
            echo "Build failed at stage — check the logs above."
        }
        always {
            cleanWs()
        }
    }
    // post {
    //     success {
    //          setGitHubPullRequestStatus state: 'SUCCESS'
    //     }
    //     failure {
    //          setGitHubPullRequestStatus state: 'FAILURE'
    //     }
    // }
}
