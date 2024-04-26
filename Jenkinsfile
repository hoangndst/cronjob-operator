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
                sh 'golangci-lint run --out-format=colored-line-number'
            }
        }
    }
}
