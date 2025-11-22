pipeline {
    agent any

    /* Environment Variables step */
    environment {
        VERSION = '1.0.0'
        APP_NAME = 'MyJenkinsApp'
    }

    stages {

        stage('Build') {
            steps {
                echo "Building version ${VERSION} of ${APP_NAME}..."
            }
        }

        stage('Test') {
            steps {
                echo "Testing version ${VERSION}..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ${APP_NAME} version ${VERSION}..."
            }
        }
    }

    post {
        always {
            echo "Pipeline Completed (version ${VERSION})"
        }
    }
}
