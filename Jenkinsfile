pipeline {
    agent {
        label 'operator-jenkins-agent'
    }
    stages {
        stage('golangci-lint') {
            steps {
                sh 'golangci-lint linters'
                sh 'golangci-lint run --out-format=colored-line-number'
            }
        }
    }
}
