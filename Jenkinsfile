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
        stage('Test') {
            steps {
                sh 'make test'
            }
        }
    }
}
