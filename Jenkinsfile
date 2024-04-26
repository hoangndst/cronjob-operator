pipeline {
    agent {
        label 'operator-jenkins-agent'
    }

    stages {
        stage('Check go version') {
            steps {
                sh 'go version'
            }
        }
        stage('golangci-lint') {
            steps {
                sh 'golangci-lint run --out-format=colored-line-number'
            }
        }
    }
}
