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
                    sh './out'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deployed :)'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}