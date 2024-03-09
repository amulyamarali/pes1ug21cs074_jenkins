pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build "pes1ug21cs121-1"
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