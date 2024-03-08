pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                   
                    sh 'g++ task_5.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy :)'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}