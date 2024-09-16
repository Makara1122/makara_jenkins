pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git url: 'https://github.com/Makara1122/makara_jenkins.git', branch: 'main'
            }
        }
        stage('List Files') {
            steps {
                // List the files in the workspace
                sh 'ls -lrt'
            }
        }
        stage('Check Git Version') {
            steps {
                // Print the Git version
                sh 'git --version'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
