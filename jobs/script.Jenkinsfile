def userName="ouliangfei"

node {
    echo "hello ${userName}"
    echo "${env.JOB_NAME} Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
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