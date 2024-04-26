pipeline {
    agent {
        label 'operator-jenkins-agent'
    }

    stages {
        stage('Set up Go environment') {
            steps {
                script {
                    env.PATH = "/usr/local/go/bin:${env.PATH}"
                }
            }
        }
        stage('golangci-lint') {
            steps {
                sh 'golangci-lint run --out-format=colored-line-number'
            }
        }
    }
}
