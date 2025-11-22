pipeline {
    agent any

    /* Step: Add Maven build tool */
    tools {
        maven 'maven'   // This name MUST match Jenkins Tools configuration
    }

    /* Environment variables from previous step */
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

        /* NEW REQUIRED STEP: Maven Build */
        stage('Maven Version Check') {
            steps {
                // Windows uses 'bat', Linux/Mac uses 'sh'
                bat 'mvn -version'
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
