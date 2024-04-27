pipeline {
    agent {
        label 'operator-jenkins-agent'
    }
    environment {
        PATH = "/usr/local/go/bin:${PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                sh 'make lint'
            }
        }
        stage('Format') {
            steps {
                sh 'make fmt'
            }
        }
        stage('Test') {
            steps {
                sh 'make test'
            }
        }
        stage('Test e2e') {
            steps {
                sh 'make test-e2e'
            }
        }
    }
}
