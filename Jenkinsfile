pipeline {
    agent {
        label 'operator-jenkins-agent'
    }
    stages {
        stage('golangci-lint') {
            steps {
                sh 'export PATH=$PATH:/usr/local/go/bin'
                sh 'golangci-lint linters'
                sh 'golangci-lint run --out-format=colored-line-number'
            }
        }
    }
}
