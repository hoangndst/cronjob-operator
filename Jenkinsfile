pipeline {
    agent {
        label 'dynamic-agent'
    }
    tools {
        go 'go-1.21'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'go version'
            }
        }
    }
}
