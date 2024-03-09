pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
              build 'PES2UG21CS120-1'
              sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
              sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echooo 'Deploying...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
