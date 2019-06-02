node {
    
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