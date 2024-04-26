pipeline {
    agent {
        label 'operator-jenkins-agent'
    }
    stages {
        stage('golangci-lint') {
            steps {
                sh 'golangci-lint run --config ".golangci.yml" --out-format=colored-line-number'
            }
        }
    }
}
