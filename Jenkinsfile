pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                   
                    sh 'g++ working.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './non_existent_executable'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}