pipeline {
    agent any
    tools {
        go 'go-1.16'
    }
    environment {
        GO111MODULE = 'on'
    }
    stages {
        stage('Build') {
            steps {
                sh 'go build'
            }
        }
    stage('Code Analysis') {
            steps {
                sh '/usr/local/bin/sl analyze --app GoLangShiftLeft --go --cpg ./...'
               
            }
       }
    }
}
