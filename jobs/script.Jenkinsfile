node {
    
    try {
        checkout scm
        stage('Build') {
            archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            echo 'Building....'
        }
        stage('Test') {
            sh 'make check || true' 
            junit '**/target/*.xml' 
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