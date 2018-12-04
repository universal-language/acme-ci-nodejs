#!groovy

node {
    stage('Checkout') {
        checkout scm
    }
    stage('Build Images') {
        awsCodeBuild projectName: 'acme-ci-nodejs', credentialsType: 'keys', region: 'us-east-1', sourceControlType: 'jenkins'
    }
}
