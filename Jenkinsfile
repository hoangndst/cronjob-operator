pipeline {
    agent {
        label 'operator-jenkins-agent'
    }
    stages {
        stage('golangci-lint') {
            steps {
                sh 'dir'
                sh 'golangci-lint run --config "cronjob-operator/.golangci.yml" --out-format=colored-line-number'
            }
        }
    }
}
