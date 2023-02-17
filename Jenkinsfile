pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp'
                build job: 'PES2UG20CS487-1'
            }
        }
        stage('Test') {
            steps {
                sh './a.out'
                echo "Build stage successful"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployment stage"
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
}
}
}
