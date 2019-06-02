node {
    
    try {
        checkout scm
        stage('Build') {
            echo 'Building....'
        }
        stage('Test') {
            echo 'Building....'
        }
        stage('Deploy') {
            echo 'Deploying....'
            sh './home/script/deploy.sh'
        } 
    } finally {
        post {
            always {
                echo 'One way or another, I have finished'
                /* clean up our workspace */
            }
            success {
                echo 'I succeeeded!'
            }
            unstable {
                echo 'I am unstable :/'
            }
            failure {
                echo 'I failed :('
            }
            changed {
                echo 'Things were different before...'
            }
        }
    } 
}