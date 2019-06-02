pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
            node ('master'){
                echo 'Building....'
            }
        }
        }
        stage('Test') {
            steps {
            node ('master'){
                echo 'Test....'
            }
        }
        }
        stage('Deploy') {
            steps {
            node ('master'){
                echo 'Deploying....'
        }
        }
        stage('Send Email') {
            steps {
            node ('master'){
                echo 'Send Email'
            }
        }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello!'
        }
        aborted {
            echo 'I was aborted'
        }
        failure {
            mail to: '2925807448@qq.com',
            subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
            body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}