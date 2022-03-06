pipeline {
    agent any

    stages {
        stage("Build") {
            steps{
                echo("Building the app")
            }
        }
        stage("test") {
            when {
                expression {
                    BRANCH_NAME == "dev"
                }
            }
            steps{
                echo("testing the app in the dev branch")
            }
        }
         stage("deploy") {
            steps{
                echo("deploying the app")
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