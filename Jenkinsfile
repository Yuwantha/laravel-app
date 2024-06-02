pipeline {
    agent any
    environment {
        DIRECTORY_PATH = "C:\\Users\\Yuwantha\\Desktop\\My\\laravel-app"
        TESTING_ENVIRONMENT = "testing"
        PRODUCTION_ENVIRONMENT = "yourname_production"
    }
    stages {
        stage('Build') {
            steps {
                script {
                    echo "Fetch the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                    echo "Compile the code and generate any necessary artifacts"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "Unit tests"
                    echo "Integration tests"
                }
            }
        }
        stage('Code Quality Check') {
            steps {
                script {
                    echo "Check the quality of the code"
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo "Deploy the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
                }
            }
        }
        stage('Approval') {
            steps {
                script {
                    echo "Waiting for manual approval"
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo "Deploy the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
                }
            }
        }
    }
}
