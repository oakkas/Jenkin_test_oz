pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                echo "Building the app at ${BRANCH_NAME}"
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