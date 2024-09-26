pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/Govind-M/NewGit-Practice5'
        DESTINATION_FOLDER = '/home/govind/Jenkins_Assignment-1'
    }

    stages {
        stage('Git Checkout') {
            steps {
                // Clone all branches
                sh '''
                rm -rf ${DESTINATION_FOLDER}
                git clone ${GIT_REPO} ${DESTINATION_FOLDER}
                '''
            }
        }
    }

    post {
        always {
            // Clean up the workspace
            cleanWs()
        }
    }
}
