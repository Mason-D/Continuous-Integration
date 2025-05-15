pipeline{
    agent any

    environment {
        DIRECTORY_PATH = 'C:/ProgramData/Jenkins/.jenkins/workspace'
        TESTING_ENVIRONMENT = 'Continuous Integration'
        PRODUCTION_ENVIRONMENT = 'Mason Dixon'
    }

    stages{
        
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable: $DIRECTORY_PATH"
                echo "Compile the code and generate any necessary artefacts"
            }
        }

        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable: $TESTING_ENVIRONMENT"
            }
        }

        stage('Approval') {
            steps {
                sleep 10
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to the production environment: $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}