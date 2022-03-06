pipeline {
    agent any

    stages {
        stage("Build") {
            steps{
                echo("Building the app")
            }
        }
        stage("test") {
            steps{
                echo("testing the app")
            }
        }
         stage("deploy") {
            steps{
                echo("deploying the app")
                throw new Exception("Failed to deploy")
            }
        }
    }
    post{
        always{
            echo "this is a msg from always Block"
        }
        success{
            echo "successfully completed"
        }
        failure{
            echo("failed")
        }
    }
}