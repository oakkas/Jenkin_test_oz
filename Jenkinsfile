pipeline{
    agent any
    environment{
        GITHUB_CREDS = credentials("github_creds")
    }
    stages{
        stage("build"){
            steps{
                echo "Building the app at ${BRANCH_NAME}"
                echo "EXECUTOR_NUMBER: ${EXECUTOR_NUMBER}"
                echo "NODE_NAME: ${NODE_NAME}"
                echo "WORKSPACE: ${WORKSPACE}"
                echo "WORKSPACE_TMP: ${WORKSPACE_TMP}"
                echo "GITHUB CREDS: ${GITHUB_CREDS}"
            }
        }
        stage("test"){
            steps{
                echo "Testing the app at ${BRANCH_NAME}"
            }
        }
        stage("deploy"){
            steps{
                echo "Deploying the app at ${BRANCH_NAME}"
            }
        }
    }
}