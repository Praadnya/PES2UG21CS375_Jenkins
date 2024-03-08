pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS375-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output_file'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
