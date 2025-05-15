pipeline{
    agent any

    environment {
        DIRECTORY_PATH = 'Continuous-Integration'
    }

    stages{
        
        stage('Build') {
            steps {
                echo "Building from $DIRECTORY_PATH"
            }
            post{
                always{
                    mail to: "unicornomoe@gmail.com",
                    subject: "Build Status Email",
                    body: "Build log attached!"
                }
            }
        }

        stage('Test') {
            steps {
                echo "Unit and Integration testing..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy the application"
            }
        }

        stage("Completed."){
            steps{
                echo "Completed"
            }
        }
        
    }
}
