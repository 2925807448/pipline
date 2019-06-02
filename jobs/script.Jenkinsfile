def userName="ouliangfei"
properties([parameters([string(defaultValue: 'Hello', description: 'How should I greet the world?', name: 'Greeting')])])

node {
    echo "hello ${userName}"
    echo "${env.JOB_NAME} Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
    echo "${params.Greeting} World!"
    try {
        checkout scm
        stage('Build') {
            echo 'Building....'
        }
        stage('Test') {
            echo 'Test....'
        }
        stage('Deploy') {
            if (currentBuild.result == null || currentBuild.result == 'SUCCESS') { 
                echo 'Deploying....'
            }
        } 
    } finally {
        echo 'Finish....'
    } 
}